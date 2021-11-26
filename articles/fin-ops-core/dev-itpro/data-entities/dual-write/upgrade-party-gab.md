---
title: อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
description: หัวข้อนี้จะอธิบายวิธีการอัปเกรดข้อมูลแบบสองทิศทางให้กับรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 6ed2a8a06b9a026a47ee8bee62aeb63bd64291ef
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783075"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[แม่แบบ Microsoft Azure Data Factory](https://aka.ms/dual-write-gab-adf) ช่วยคุณในการอัปเกรดข้อมูลตาราง **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** แบบสองทิศทางให้กับไปยังรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล แม่แบบจะกระทบยอดข้อมูลจากทั้งแอป Finance and Operations และแอปการมีส่วนร่วมกับลูกค้า เมื่อสิ้นสุดกระบวนการ ฟิลด์ **ฝ่าย** และ **ผู้ติดต่อ** ของเรกคอร์ด **ฝ่าย** จะมีการสร้างและเชื่อมโยงกับเรกคอร์ด **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมกับลูกค้า ไฟล์ .csv (`FONewParty.csv`) ถูกสร้างขึ้นเพื่อสร้างเรกคอร์ด **ฝ่าย** ใหม่ภายในแอป Finance and Operations หัวข้อนี้จะให้คําแนะนําในการใช้แม่แบบ Data Factory และอัปเกรดข้อมูลของคุณ

ถ้าคุณไม่มีการกำหนดใด ๆ คุณสามารถใช้แม่แบบตามที่เป็นได้ ถ้าคุณมีการกำหนดสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** จากนั้นคุณต้องปรับเปลี่ยนแม่แบบโดยใช้คําแนะนําต่อไปนี้

> [!NOTE]
> แม่แบบจะอัปเกรดเฉพาะข้อมูล **ฝ่าย** ในการนำออกใช้ในอนาคต ที่อยู่ไปรษณีย์และที่อยู่อิเล็กทรอนิกส์จะถูกรวมไว้ด้วย

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ข้อเบื้องต้นต่อไปนี้จำเป็นเพื่ออัปเกรดเป็นแบบโมเดลฝ่ายและสมุดที่อยู่สากล:

+ [การบอกรับเป็นสมาชิก Azure](https://portal.azure.com/)
+ [เข้าถึงแม่แบบ](https://aka.ms/dual-write-gab-adf)
+ คุณต้องเป็นลูกค้าการรวมแบบสองทิศทางที่มีอยู่

## <a name="prepare-for-the-upgrade"></a>จัดเตรียมสำหรับการอัปเกรด
กิจกรรมต่อไปนี้ต้องเตรียมการเพื่อเตรียมการอัปเกรด

+ **ซิงค์อย่างครบถ้วน**: ทั้งสองสภาพแวดล้อมอยู่ในสถานะถูกซิงค์อย่างครบถ้วนแล้วสำหรับ **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**
+ **คีย์การรวม**: ตาราง **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมกับลูกค้าใช้คีย์การรวมที่จัดส่งแบบสำเร็จรูป ถ้าคุณเลือกกำหนดคีย์การรวมเอง คุณต้องเลือกกำหนดแม่แบบเอง
+ **หมายเลขฝ่าย**: เรกคอร์ด **บัญชี (ลูกค้า)** ทั้งหมด **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ที่จะอัปเกรดมีหมายเลข **ฝ่าย** เรกคอร์ดที่ไม่มีหมายเลข **ฝ่าย** จะถูกละเว้น ถ้าคุณต้องการอัปเกรดเรกคอร์ดเหล่านั้น ให้เพิ่มหมายเลข **ฝ่าย** ก่อนที่คุณจะเริ่มกระบวนการอัปเกรด
+ **ความขัดข้องของระบบ**: ในระหว่างกระบวนการอัปเกรด คุณจะต้องใช้ทั้งสภาพแวดล้อม Finance and Operations และการมีส่วนร่วมกับลูกค้าออฟไลน์
+ **สแนปช็อต**: ถ่ายภาพสแนปช็อตของทั้งแอป Finance and Operations และแอปการมีส่วนร่วมกับลูกค้า ใช้สแนปช็อตเพื่อคืนสถานะก่อนหน้านี้ถ้าคุณต้องการ

## <a name="deployment"></a>การจัดวาง

1. ดาวน์โหลดแม่แบบจาก [Dynamics-365-FastTrack-Implementation-Assets](https://aka.ms/dual-write-gab-adf)

2. ลงชื่อเข้าใช้ [Microsoft Azure](https://portal.azure.com/)

3. สร้าง [กลุ่มทรัพยากร](/azure/azure-resource-manager/management/manage-resource-groups-portal)

4. สร้าง [บัญชีการจัดเก็บ](/azure/storage/common/storage-account-create?tabs=azure-portal) ในกลุ่มทรัพยากรที่คุณสร้างขึ้น

5. สร้าง [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) เหนือกลุ่มทรัพยากรที่คุณสร้างขึ้น

6. เปิด Data Factory และเลือกไทล์ **สร้าง & ตรวจสอบ**

7. บนแท็บ **จัดการ** ให้เลือก **แม่แบบ ARM**

8. เลือกแม่แบบ **นำเข้าแม่แบบ ARM** เพื่อนําเข้าแม่แบบ **ฝ่าย**

9. นําเข้าแม่แบบไปยัง Data Factory ป้อนค่าต่อไปนี้ให้กับ **รายละเอียดโครงการ** และ **รายละเอียดอินสแตนซ์**

    ฟิลด์ | มูลค่า
    ---|---
    การบอกรับเป็นสมาชิก | การบอกรับเป็นสมาชิก Azure
    กลุ่มทรัพยากร | ระบุทรัพยากรเดียวกันกับที่มีการสร้างบัญชีการจัดเก็บ
    ภูมิภาค | ระบุภูมิภาค
    ชื่อโรงงาน | ระบุชื่อโรงงาน
    คีย์หลัก FO ที่เชื่อมโยง Service_service | ระบุคีย์ของโปรแกรมประยุกต์
    ที่เก็บข้อมูล Azure Blob_สตริงการเชื่อมต่อ | สตริงการเชื่อมต่อที่เก็บข้อมูล Azure Blob
    Dynamics Crm ที่เชื่อมโยง Service_password | รหัสผ่านของบัญชีผู้ใช้ที่คุณระบุเป็นชื่อผู้ใช้
    FO Linked Service_properties_type Properties_url  | `https://sampledynamics.sandbox-operationsdynamics.com/data`
    FO Linked Service_properties_type Properties_tenant | ระบุข้อมูลผู้เช่า (ชื่อโดเมนหรือรหัสผู้เช่า) ที่โปรแกรมประยุกต์ของคุณอยู่
    FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com`
    FO Linked Service_properties_type Properties_service Principal Id | ระบุรหัสไคลเอนต์ของโปรแกรมประยุกต์
    Dynamics Crm Linked Service_properties_type Properties_username | ชื่อผู้ใช้ที่จะเชื่อมต่อกับ Dynamics 365

    สำหรับข้อมูลเพิ่มเติม โปรดดูหัวข้อต่อไปนี้ 
    
    - [เลื่อนระดับแม่แบบ Resource Manager ด้วยตนเองในแต่ละสภาพแวดล้อม](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [คุณสมบัติของบริการที่เชื่อมโยง](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [คัดลอกข้อมูลโดยใช้ Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. หลังจากใช้งานแล้ว ให้ตรวจสอบความถูกต้องของชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยงของ Data Factory

   ![ชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยง](media/data-factory-validate.png)

11. นําทางไปยัง **จัดการ** ภายใต้ **การเชื่อมต่อ** ให้เลือก **บริการที่เชื่อมโยง** เลือก **DynamicsCrmLinkedService** ในฟอร์ม **แก้ไขบริการที่เชื่อมโยง (Dynamics CRM)** ให้ป้อนค่าต่อไปนี้

    ฟิลด์ | มูลค่า
    ---|---
    ชื่อ | DynamicsCrmLinkedService
    คำอธิบาย | บริการที่เชื่อมโยงเพื่อเชื่อมต่อกับอินสแตนซ์ CRM เพื่อดึงข้อมูลเอนทิตีมาใช้
    เชื่อมต่อผ่าน Integration Runtime | AutoResolvelntegrationRuntime
    ชนิดการปรับใช้ | ออนไลน์
    Uri ของการบริการ | `https://<organization-name>.crm[x].dynamics.com`
    ชนิดการรับรองความถูกต้อง | Office365
    ชื่อผู้ใช้ |
    รหัสผ่านหรือ Azure Key Vault | รหัสผ่าน
    รหัสผ่าน |

## <a name="run-the-template"></a>เรียกใช้แม่แบบ

1. หยุดแม็ปการรวมแบบสองทิศทาง **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ต่อไปนี้โดยใช้แอป Finance and Operations

    + Customers V3 (บัญชี)
    + ลูกค้า V3(ผู้ติดต่อ)
    + ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)
    + ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)
    + ผู้จัดจำหน่าย V2 (msdyn_vendor)

2. ตรวจสอบให้แน่ใจว่าแผนที่ถูกลบออกจากตาราง `msdy_dualwriteruntimeconfig` ใน Dataverse

3. ติดตั้ง [ฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากล](https://aka.ms/dual-write-gab) จาก AppSource

4. ในแอป Finance and Operations หากตารางต่อไปนี้มีข้อมูล ให้รัน **การซิงค์ครั้งแรก**

    + คำขึ้นต้น
    + ชนิดลักษณะส่วนบุคคล
    + คำลงท้าย
    + ตำแหน่งของผู้ติดต่อ
    + บทบาทในการตัดสินใจ
    + ระดับของสมาชิก

5. ในแอปการมีส่วนร่วมกับลูกค้า ให้ปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้

    + การอัปเดตบัญชี
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี
    + การอัปเดตผู้ติดต่อ
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ
    + อัปเดต msdyn_party
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party
    + การอัปเดต msdyn_vendor
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor

6. ในแอปการมีส่วนร่วมกับลูกค้า ให้ปิดใช้งานลำดับงานต่อไปนี้:

    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายในตารางบัญชี
    + อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย

7. ใน Data Factory ให้รันแม่แบบโดยการเลือก **ทริกเกอร์ตอนนี้** ดังที่แสดงในภาพต่อไปนี้ กระบวนการนี้อาจใช้เวลาสักครู่เพื่อกรอกข้อมูลตามปริมาณข้อมูล

    ![การรันทริกเกอร์](media/data-factory-trigger.png)

    > [!NOTE]
    > ถ้าคุณมีการกำหนดสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** จากนั้นคุณต้องปรับเปลี่ยนแม่แบบ

8. นําเข้าเรกคอร์ด **ฝ่าย** ในแอป Finance and Operations

    + ดาวน์โหลดไฟล์ `FONewParty.csv` จากที่จัดเก็บ Azure blob พาธคือ `partybootstrapping/output/FONewParty.csv`
    + แปลงไฟล์ `FONewParty.csv` เป็นไฟล์ Excel และนําเข้าไฟล์ Excel ไปยังแอป Finance and Operations หากการนําเข้า csv ใช้ได้ คุณสามารถนําเข้าไฟล์ csv ได้โดยตรง การนําเข้าอาจใช้เวลาสองสามชั่วโมงในการรัน ทั้งนี้ขึ้นอยู่กับปริมาณข้อมูล สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](../data-import-export-job.md)

    ![นําเข้าเรกคอร์ดฝ่ายของ Datavers](media/data-factory-import-party.png)

9. ในแอปการมีส่วนร่วมกับลูกค้า ให้เปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้:

    + การอัปเดตบัญชี
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี
    + การอัปเดตผู้ติดต่อ
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ
         + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ
    + อัปเดต msdyn_party
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party
    + การอัปเดต msdyn_vendor
         + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor

10. ในแอปการมีส่วนร่วมกับลูกค้า ให้เรียกใช้ลำดับงานต่อไปนี้ หากคุณยกเลิกการเรียกใช้ในขั้นตอนก่อนหน้า:

    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายในตารางบัญชี
    + อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย

11. รันแผนผังที่เกี่ยวข้องกับ **ฝ่าย** ตามที่สั่งใน [สมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล](party-gab.md)

## <a name="troubleshooting"></a>การแก้ไขปัญหา

1. ถ้ากระบวนการล้มเหลว ให้รัน Data Factory ใหม่เริ่มต้นจากกิจกรรมที่ล้มเหลว
2. บางไฟล์จะถูกสร้างขึ้นโดย Data Factory ที่คุณสามารถใช้เพื่อวัตถุประสงค์การตรวจสอบความถูกต้องของข้อมูล
3. Data Factory จะรันตามไฟล์ csv ที่คั่นด้วยเครื่องหมายจุลภาค ถ้ามีค่าฟิลด์ที่มีเครื่องหมายจุลภาค อาจใช้เฉพาะกับผลลัพธ์ คุณต้องลบเครื่องหมายจุลภาค
4. แท็บ **การตรวจสอบ** แสดงข้อมูลเกี่ยวกับขั้นตอนและข้อมูลทั้งหมดที่ประมวลผล เลือกขั้นตอนเฉพาะเพื่อดีบักขั้นตอนนั้น

    ![แท็บการตรวจสอบ](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>เรียนรู้เพิ่มเติมเกี่ยวกับแม่แบบ

คุณสามารถค้นหาข้อมูลเพิ่มเติมเกี่ยวกับแม่แบบใน [ข้อคิดเห็นสำหรับ readme ของแม่แบบ Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)
