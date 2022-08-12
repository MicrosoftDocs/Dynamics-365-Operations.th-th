---
title: เพิ่มประสิทธิภาพการสอบถามตารางเสมือน Dataverse
description: เพิ่มประสิทธิภาพและแก้ไขปัญหาประสิทธิภาพของการสอบถามตารางเสมือน Dataverse
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f379cd7783cc984666582d2c680a1db013627ce
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070186"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>เพิ่มประสิทธิภาพการสอบถามตารางเสมือน Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>ออก

### <a name="overview"></a>ภาพรวม

เมื่อใช้ตารางเสมือน Dataverse เพื่อพัฒนาการรวมและการเชื่อมต่อข้อมูลอื่น ๆ ด้วย Dynamics 365 Human Resources คุณสามารถพบปัญหาเกี่ยวกับประสิทธิภาพการสอบถามกับตารางเสมือนได้ การปฏิบัติการสอบถามแบบช้าอาจเกิดขึ้นระหว่างไคลเอนต์หรืออินเทอร์เฟสต่าง ๆ ตัวอย่างเช่น คุณอาจประสบกับปัญหาในสถานการณ์ต่อไปนี้:

- เมื่อสอบถามตารางเสมือนผ่าน API ของเว็บ Dataverse
- เมื่อสร้าง Power App กับตารางเสมือน
- เมื่อสร้างรายงาน Power BI ในตารางเสมือน

อินเทอร์เฟสเหล่านี้ทั้งหมดอาจมีปัญหาด้านประสิทธิภาพ

สาเหตุหนึ่งของประสิทธิภาพการทำงานช้ากับตารางเสมือน Dataverse ของทรัพยากรบุคคลคือ คอลัมน์คีย์นอกของตารางเสมือนที่เกี่ยวข้องกับ [คุณสมบัติการนําทาง](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) ของตาราง เมื่อสร้างคุณสมบัติการนําทางให้กับตารางเสมือน คอลัมน์คีย์นอกจะถูกเพิ่มเข้าในตารางโดยอัตโนมัติเพื่อแสดงค่าของคีย์ของคอลัมน์คีย์ของตารางเสมือนที่เกี่ยวข้อง ตัวอย่างเช่น คอลัมน์ **_mshr_fk_person_id_value** จะถูกเพิ่มเข้าในเอนทิตี **mshr_hcmworkerbaseentity** กับคุณสมบัติคีย์นอกจากเอนทิตี **mshr_dirpersonentity** เนื่องจากวิธีที่เก็บรักษาค่าสำหรับคีย์นอกเหล่านี้ในตารางเสมือน การดึงข้อมูลค่าอาจมีผลกระทบในทางลบต่อประสิทธิภาพของการสอบถามกับตารางเสมือน

### <a name="potential-symptoms"></a>อาการที่เป็นไปได้

ตัวอย่างที่คุณอาจเห็นผลกระทบนี้อยู่ในการสอบถามเกี่ยวกับผู้ปฏิบัติงาน (**mshr_hcmworkerentity**) หรือเอนทิตีผู้ปฏิบัติงานพื้นฐาน (**mshr_hcmworkerbaseentity**) คุณอาจเห็นตัวรายการปัญหาประสิทธิภาพในสองสามวิธีต่อไปนี้:

- **การดําเนินการสอบถามช้า**: การสอบถามกับตารางเสมือนอาจส่งคืนผลลัพธ์ที่คาดไว้ แต่ใช้เวลานานกว่าที่คาดไว้ในการดําเนินการการสอบถามให้เสร็จสมบูรณ์
- **การหมดเวลาของการสอบถาม**: การสอบถามอาจหมดเวลาและส่งคืนข้อผิดพลาดต่อไปนี้: "ได้รับโทเค็นเพื่อเรียกการเงินและการดำเนินงาน แต่การเงินและการดำเนินงานส่งคืนข้อผิดพลาดชนิด InternalServerError"
- **ข้อผิดพลาดที่ไม่คาดคิด**: การสอบถามอาจส่งคืนชนิดข้อผิดพลาด 400 พร้อมด้วยข้อความต่อไปนี้: "เกิดข้อผิดพลาดที่ไม่คาดคิด"

  ![ชนิดข้อผิดพลาด 400 บน HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- **การควบคุมปริมาณ**: การสอบถามอาจใช้ทรัพยากรเซิร์ฟเวอร์มากเกินไปและอยู่ภายใต้การควบคุมปริมาณ ในกรณีนี้ การสอบถามจะส่งคืนข้อผิดพลาดต่อไปนี้: "ได้รับโทเค็นเพื่อเรียกการเงินและการดำเนินงาน แต่การเงินและการดำเนินงาน ส่งคืนข้อผิดพลาดชนิด 429" หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับการควบคุมปริมาณในทรัพยากรบุคคล โปรดดูที่ [คำถามที่ถามบ่อยเกี่ยวกับการควบคุมปริมาณ](./hr-admin-integration-throttling-faq.md)

  ![ชนิดข้อผิดพลาด 429 บน HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>การแก้ปัญหา

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>การจํากัดจํานวนคอลัมน์ที่รวมอยู่ในการสอบถามข้อมูลของคุณ

ด้วยตารางเสมือน วิธีการใดตารางหนึ่งที่มีความเป็นไปได้มากที่สุดในการปรับปรุงประสิทธิภาพของการสอบถาม คือจํากัดจํานวนคอลัมน์ที่เลือกในการสอบถาม แนวทางทั่วไปสําหรับการเพิ่มประสิทธิภาพประสิทธิภาพของการสอบถาม คือจํากัดคอลัมน์ที่ส่งคืนในการสอบถามของคุณไปยังเฉพาะคุณสมบัติที่คุณต้องการ โดยเฉพาะอย่างยิ่งกับคอลัมน์คีย์นอกในตารางเสมือน ถ้าคุณไม่ต้องการค่าในคอลัมน์คีย์นอกเพื่อการรวมหรือรายงานของคุณ ให้จัดโครงสร้างการสอบถามเพื่อเลือกเฉพาะคอลัมน์ที่คุณต้องการ โดยไม่รวมคอลัมน์คีย์นอก

#### <a name="selecting-columns-in-an-odata-query"></a>การเลือกคอลัมน์ในการสอบถาม OData

เมื่อสอบถามตารางเสมือนผ่าน API ของเว็บ Dataverse คุณสามารถจํากัดจํานวนของคอลัมน์ที่รวมอยู่ในการสอบถามได้โดยใช้ตัวเลือกการสอบถามระบบ **$select** และกําหนดคอลัมน์ที่คุณต้องการส่งคืนผลลัพธ์ เพื่อเพิ่มประสิทธิภาพให้สูงสุด แยกคอลัมน์คีย์นอก (คอลัมน์ที่มีคำนำหน้า **_mshr_FK_**) จากการสอบถาม

ตัวอย่างเช่น การสอบถามต่อไปนี้เทียบกับเอนทิตี **mshr_hcmworkerbaseentity** จะรวมเฉพาะคอลัมน์ที่รวมอยู่ในอนุประโยคตัวเลือกการสอบถาม **$select** โดยไม่รวมค่าคีย์นอก สิ่งนี้จะให้การปรับปรุงประสิทธิภาพที่สําคัญเหนือกว่าการสอบถามที่มีคอลัมน์ตารางทั้งหมด

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

ข้อแนะนําในการจํากัดจํานวนคอลัมน์ที่เลือกยังใช้เมื่อใช้ตัวเลือกการสอบถาม **$expand** เพื่อขยายการสอบถามไปยังตารางเสมือนที่เกี่ยวข้องผ่านคุณสมบัติการนําทาง ตัวอย่างเช่น การสอบถามต่อไปนี้รวมคอลัมน์จากเอนทิตี **mshr_hcmworkerbaseentity** ที่มีคอลัมน์ขยายจากเอนทิตี **mshr_dirpersonentity** โปรดทราบว่าตัวเลือกการสอบถาม **$select** จะถูกรวมไว้ในอนุประโยคการสอบถาม **$expand** ด้วย

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

เมื่อใช้วิธีการดึงข้อมูลนี้โดยใช้ตัวเลือกการสอบถาม **$select** ในอนุประโยคตัวเลือกการสอบถาม **$expand** คุณจะเห็นการปรับปรุงประสิทธิภาพการนําทางมากขึ้นเมื่อคุณสมบัติการนําทางระหว่างเอนทิตีเป็นความสัมพันธ์แบบกลุ่มต่อหนึ่ง คุณอาจไม่เห็นการลดลงเดียวกันในเวลาการปฏิบัติการของการสอบถามเมื่อขยายความสัมพันธ์แบบหนึ่งต่อกลุ่ม หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับนิยามความสัมพันธ์สำหรับตารางเสมือน Dataverse โปรดดูที่ [ความสัมพันธ์ของตาราง](/powerapps/maker/data-platform/create-edit-entity-relationships)

หากต้องการข้อมูลเพิ่มเติมเกี่ยวกับการใช้ตัวเลือกการสอบถามของระบบ **$select** และ **$expand** ใน API ของเว็บ โปรดดูที่ [ดึงข้อมูลเรกคอร์ดเอนทิตี Dataverse ที่เกี่ยวข้องกับการสอบถาม](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query)

#### <a name="selecting-columns-in-power-bi"></a>การเลือกคอลัมน์ใน Power BI

หากคุณประสบการบ่งชี้ใด ๆ ที่กล่าวมาดังกล่าวเกี่ยวกับประสิทธิภาพการการปฏิบัติงานที่ช้าเมื่อสร้างรายงาน Power BI กับตารางเสมือน Dataverse คุณสามารถปรับปรุงประสิทธิภาพการงานได้ ด้วยการไม่รวมคอลัมน์คีย์นอกจากคอลัมน์ที่เลือกจากตารางของรายงาน ตัวอย่างเช่น ถ้าคุณจะใช้ Power BI Desktop สร้างรายงานโดยเทียบกับเอนทิตี **mshr_hcmworkerbaseentity** นี้ คุณสามารถใช้ขั้นตอนต่อไปนี้เพื่อเลือกคอลัมน์ที่คุณต้องการรวมในการสอบถามของรายงาน

1. ใน Power BI Desktop ให้เลือก **เพิ่มเติม...** จากรายการแบบหล่นลง **รับข้อมูล** บน Ribbon การดำเนินการ
2. ในหน้าต่าง **รับข้อมูล** ป้อน **Common Data Service** ในกล่องค้นหา เลือกตัวเชื่อมต่อ **Common Data Service** และเลือก **เชื่อมต่อ**
3. ในฟิลด์ **Url เซิร์ฟเวอร์** ของหน้าต่าง Common Data Service ให้ป้อน URI ขององค์กรให้กับสภาพแวดล้อม Dataverse ของคุณ และเลือก **ตกลง**
  
   ![ป้อน URI สำหรับสภาพแวดล้อม Dataverse ของคุณ](./media/PowerBIDataverseURLSetup.png)
  
4. ในหน้าต่างตัวนําทาง ให้ขยายโหนด **เอนทิตี**
5. ในกล่องค้นหา ให้ป้อน **mshr_hcmworkerbaseentity** และเลือกเอนทิตี
6. เลือก **แปลงข้อมูล**
7. ในหน้าต่างตัวแก้ไข Power Query ให้เลือก **เครื่องมือแก้ไขขั้นสูง**
8. ในหน้าต่างโปรแกรม **เครื่องมือแก้ไขขั้นสูง** ให้อัปเดตการสอบถามให้มีลักษณะเป็นด้านล่าง เพิ่มหรือลบคอลัมน์ใด ๆ ไปยังแถวลำดับที่ต้องการ

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![อัปเดตการสอบถามในฟิลด์เครื่องมือแก้ไขขั้นสูงสำหรับตัวแก้ไข Power Query](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. เลือก **เสร็จสิ้น**

   > [!NOTE]
   > ถ้าคุณได้รับข้อผิดพลาดชนิด 429 จากการสอบถามก่อนที่จะอัปเดต คุณอาจต้องรอรอบระยะเวลาการลองส่งใหม่ก่อนที่จะรีเฟรชการสอบถามเพื่อให้การการสอบถามเสร็จสมบูรณ์อย่างต่อเนื่อง

10. คลิก **ปิดและนำไปใช้** บน Ribbon การดำเนินการตัวแก้ไข Power Query

จากนั้นคุณสามารถเริ่มต้นสร้างรายงาน Power BI ของคุณโดยเทียบกับคอลัมน์ที่เลือกจากตารางเสมือนได้

#### <a name="selecting-columns-in-power-apps"></a>การเลือกคอลัมน์ใน Power Apps

คล้ายกับการสอบถาม API ของเว็บ Dataverse และ Power BI คุณสามารถปรับปรุงประสิทธิภาพการสอบถามสำหรับ Power Apps ให้ดีขึ้นได้ตามตารางเสมือน Dataverse โดยไม่รวมคอลัมน์ของตารางที่เกี่ยวข้องจากแอปของคุณ ถ้ารวมคอลัมน์ใด ๆ จากตารางที่เกี่ยวข้องบนหน้า URL คำขอที่สร้างขึ้นเพื่อดึงข้อมูลจะรวมคุณสมบัติคีย์นอกของตารางที่เกี่ยวข้องด้วย ในตัวอย่างของ [การเลือกคอลัมน์ใน OData Query](#selecting-columns-in-power-apps) ข้างต้น จะลดประสิทธิภาพโดยทําให้การค้นหาข้อมูลเพิ่มเติมลดลง

เมื่อต้องการแก้ไขปัญหานี้ คุณสามารถตรวจสอบความถูกต้องว่าไม่มีฟิลด์ข้อมูลจากตารางที่เกี่ยวข้องรวมอยู่ในฟอร์มข้อมูลใด ๆ ของ Power App ของคุณ

1. ในบานหน้าต่างมุมมองแผนภูมิ เลือกฟอร์มข้อมูลหน้าจอ
2. ในบานหน้าต่าง **คุณสมบัติ** ให้เลือก **แก้ไข** บนคุณสมบัติ **ฟิลด์**
3. ในบานหน้าต่าง **ข้อมูล** ให้ตรวจสอบว่าไม่มีฟิลด์ที่เลือกใดเป็นฟิลด์ของตารางเสมือนของแหล่งข้อมูล

ตัวอย่างเช่น ถ้าฟิลด์ใดฟิลด์หนึ่งที่รวมอยู่ในหน้าแอปอ้างอิงอีกตารางหนึ่ง เช่น **ThisItem.Worker.Name** โดยที่ **ผู้ปฏิบัติงาน** เป็นตารางที่เกี่ยวข้อง อาจมีประสิทธิภาพการลดลงในการดึงข้อมูล

คุณสามารถใช้ [Power Apps Monitor](/powerapps/maker/monitor-overview) เพื่อให้แน่ใจว่าเฉพาะคอลัมน์ที่คุณต้องการรวมอยู่ในการสอบถามเพื่อรับข้อมูลใน Power App คุณสามารถดู URL ที่สร้างไว้ให้กับการดําเนินงาน getRows เพื่อให้แน่ใจว่าคอลัมน์ที่คุณเลือกไว้เพื่อให้แอปของคุณมีประสิทธิภาพสูงสุดในการดึงข้อมูล

![ใช้ Power Apps Monitor เพื่อวิเคราะห์การดําเนินงาน getData](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>การกรองการสอบถามข้อมูล

วิธีการอื่นในการปรับปรุงประสิทธิภาพการดําเนินการสอบถามคือจํากัดจํานวนของเรกคอร์ดที่ส่งคืนในผลลัพธ์ของการสอบถาม คุณสามารถดําเนินการนี้โดยการกรองผลลัพธ์เพื่อให้แน่ใจว่าคุณจะได้รับเรกคอร์ดที่คุณต้องการเท่านั้น

ดู [ผลลัพธ์ตัวกรอง](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการกรองข้อมูลการสอบถาม

### <a name="limiting-the-page-size-of-the-query"></a>การจํากัดขนาดหน้าของการสอบถาม

ถ้าคุณใช้งานชุดข้อมูลขนาดใหญ่ คุณสามารถแบ่งผลลัพธ์ของการสอบถามออกเป็นหน้าหลายหน้าได้โดยการเพิ่มหัวข้อกำหนดลักษณะ `odata.maxpagesize` ที่การสอบถามข้อมูล

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการจัดหน้า ให้ดูที่ [ระบุจำนวนของเอนทิตีที่จะส่งคืนในหน้า](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page)

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ตั้งค่าคอนฟิกตารางเสมือน Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)
- [คำถามที่ถามบ่อยเกี่ยวกับตารางเสมือน Human Resources](hr-admin-virtual-entity-faq.md)
- [คำถามที่ถามบ่อยเกี่ยวกับการควบคุมปริมาณ](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

