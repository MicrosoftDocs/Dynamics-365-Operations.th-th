---
title: นำเข้าข้อมูลจากไฟล์ที่เลือกด้วยตนเองในโหมดชุดงาน
description: บทความนี้อธิบายวิธีการนําเข้าข้อมูลจากไฟล์ที่เลือกด้วยตนเองในโหมดชุดงาน
author: kfend
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
ms.openlocfilehash: 21a2ab5f0eb07dda92baf9cc04ee36caeff8b4ec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288242"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>นำเข้าข้อมูลจากไฟล์ที่เลือกด้วยตนเองในโหมดชุดงาน

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

หากต้องการใช้กรอบงาน [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) เพื่อนําเข้าข้อมูลจากไฟล์ขาเข้าที่เลือกด้วยตนเองในโหมดชุดงาน ให้ตั้งค่าคอนฟิก [รูปแบบ](er-overview-components.md#format-component) ER ที่รองรับการนำเข้า แล้วเรียกใช้ [การแมปแบบจำลอง](er-overview-components.md#model-mapping-component) ของชนิด **ไปยังปลายทาง** ที่ใช้รูปแบบนั้นเป็นแหล่งข้อมูล ในการนำเข้าข้อมูล เรียกดูไฟล์ที่คุณต้องการนำเข้า และเลือกด้วยตนเอง 

ความสามารถ ER ใหม่ที่สนับสนุนการนำเข้าข้อมูลในโหมดชุดงานจะเปิดใช้งานกระบวนการนี้เป็นการตั้งค่าคอนฟิกเป็นแบบอัตโนมัติ คุณสามารถใช้การตั้งค่าคอนฟิก ER เพื่อนําเข้าข้อมูลโดยการจัดกําหนดการชุดงานใหม่จากอินเทอร์เฟสผู้ใช้ ER (UI)

บทความนี้อธิบายวิธีการนําเข้าข้อมูลจากไฟล์ที่เลือกด้วยตนเองในโหมดชุดงาน ตัวอย่างใช้ธุรกรรมผู้จัดจำหน่ายเป็นข้อมูลธุรกิจ ขั้นตอนของตัวอย่างเหล่านี้สามารถดำเนินการให้เสร็จสมบูรณ์ในบริษัท **USMF** ไม่จำเป็นต้องมีการเขียนโค้ด

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

เพื่อทำตัวอย่างในบทความนี้ให้เสร็จสมบูรณ์ คุณต้องมีการเข้าถึงต่อไปนี้:

- หนึ่งในบทบาทต่อไปนี้:

    - นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
    - ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
    - ผู้ดูแลระบบ

- รูปแบบและการตั้งค่าคอนฟิกแบบจำลอง ER สำหรับการชำระเงิน 1099

### <a name="create-the-required-er-configurations"></a>สร้างการตั้งค่าคอนฟิก ER ที่จำเป็น

เมื่อต้องการสร้างการตั้งค่าคอนฟิก ER ที่กําหนดและขอข้อกําหนดเบื้องต้นอื่น ให้ปฏิบัติตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้

- เล่นคู่มืองาน **ER นำเข้าข้อมูลจากไฟล์ Microsoft Excel** ซึ่งเป็นส่วนหนึ่งของกระบวนการทางธุรกิจ **7.5.4.3 รับ/พัฒนาองค์ประกอบบริการ/โซลูชันด้าน IT (10677)** คู่มืองานเหล่านี้นำคุณไปสู่กระบวนการของการออกแบบและการใช้การตั้งค่าคอนฟิก ER เพื่อนำเข้าธุรกรรมผู้จัดจำหน่ายจากไฟล์ Microsoft Excel ในระหว่างกัน สำหรับข้อมูลเพิ่มเติม ดู [แยกวิเคราะห์เอกสารขาเข้าในรูปแบบ Excel](parse-incoming-documents-excel.md)
- ดำเนินการตามตัวอย่างใน [ตั้งค่าคอนฟิกการนำเข้าข้อมูลจาก SharePoint](er-configure-data-import-sharepoint.md) ตัวอย่างเหล่านี้นำคุณไปสู่กระบวนการของการออกแบบและการใช้การตั้งค่าคอนฟิก ER เพื่อนำเข้าธุรกรรมผู้จัดจำหน่ายจากไฟล์ Excel ที่จัดเก็บไว้ในโฟลเดอร์ SharePoint

### <a name="download-the-required-er-configurations"></a>ดาวน์โหลดการตั้งค่าคอนฟิก ER ที่จำเป็น

1. ดาวน์โหลดการตั้งค่าคอนฟิก ER ต่อไปนี้และบันทึกไว้ภายในเครื่อง

    | คำอธิบายเนื้อหา | ไฟล์ |
    |---------------------|------|
    | การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER สำหรับ **รูปแบบการชำระเงิน 1099** | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | การตั้งค่าคอนฟิกรูปแบบ ER **สำหรับการนำเข้าธุรกรรมของผู้จัดจำหน่าย (Excel)** | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. ใช้ตัวเลือก ER [โหลดจากไฟล์ XML](er-defer-sequence-element.md#import-the-sample-er-configurations) เพื่อนําเข้าการตั้งค่าคอนฟิก ER ที่ดาวน์โหลดมาไปยังอินสแตนซ์ Dynamics 365 Finance ของคุณ ในลำดับต่อไปนี้:

    1. การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER
    2. การตั้งค่าคอนฟิกรูปแบบ ER

### <a name="download-the-required-excel-files"></a>ดาวน์โหลดไฟล์ Excel ที่จำเป็น

- ดาวน์โหลดชุดข้อมูลตัวอย่างต่อไปนี้และบันทึกไว้ภายในเครื่อง

    | คำอธิบายเนื้อหา | ไฟล์ |
    |---------------------|------|
    | ไฟล์ **1099import-data.xlsx** ขาเข้าที่มีข้อมูลตัวอย่างสำหรับนำเข้า | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>ตรวจสอบข้อกำหนดเบื้องต้น

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. บนหน้า **การตั้งค่าคอนฟิก** ตรวจสอบโซลูชัน ER ที่จัดเตรียมไว้สำหรับการนําเข้าข้อมูลในโหมดชุดงาน
3. ตรวจสอบการตั้งค่าคอนฟิกรูปแบบ **สำหรับการนำเข้าธุรกรรมของผู้จัดจำหน่าย (Excel)**

    - ส่วนประกอบรูปแบบของการตั้งค่าคอนฟิกนี้ได้รับการออกแบบเพื่อแยกวิเคราะห์ไฟล์ Excel ขาเข้า
    - ส่วนประกอบการแมปรูปแบบของการตั้งค่าคอนฟิกนี้ใช้เพื่อเติมในแบบจำลองข้อมูลพื้นฐานโดยใช้ข้อมูลจากไฟล์ Excel ที่แยกวิเคราะห์

    ![การตั้งค่าคอนฟิกรูปแบบ ER สำหรับการนําเข้าข้อมูลในโหมดชุดงานจาก ER UI](./media/er-configure-data-import-batch-configurations-1.png)

4. ตรวจสอบการตั้งค่าคอนฟิกแบบจำลองข้อมูล **รูปแบบการชำระเงิน 1099**

    - ส่วนประกอบรูปแบบของการตั้งค่าคอนฟิกนี้แสดงโครงสร้างของแบบจำลองข้อมูลที่ใช้ส่งผ่านข้อมูลระบบส่วนประกอบ ER ที่ทำงาน
    - ส่วนประกอบการแมปรูปแบบของการตั้งค่าคอนฟิกนี้ใช้เพื่อดึงข้อมูลจากส่วนประกอบรูปแบบที่ปฏิบัติการแล้วและอัปเดตตารางของแอปพลิเคชัน

    ![การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER สำหรับการนําเข้าข้อมูลในโหมดชุดงานจาก ER UI](./media/er-configure-data-import-batch-configurations-2.png)

5. เปิดไฟล์ **1099import-data.xlsx** ใน Excel

    ![ตัวอย่างไฟล์ Excel ที่มีข้อมูลการนําเข้าในโหมดชุดงาน](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>เปิดใช้งานการนําเข้าข้อมูลชุดงานสำหรับ ER จาก UI

1. ไปที่ **ผู้ดูแลระบบ** \> **พื้นที่ทำงาน** \> **การจัดการลักษณะการทำงาน**
2. ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เลือกคุณลักษณะ **เรียกใช้การนำเข้า ER ของเอกสารที่อัปโหลดด้วยตนเองเป็นชุดงาน** แล้วเลือก **เปิดใช้งานทันที**

## <a name="import-data-from-manually-selected-excel-files"></a>นำเข้าข้อมูลจากไฟล์ Excel ที่เลือกด้วยตนเอง

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. บนหน้า **การตั้งค่าคอนฟิก** ให้เลือกการตั้งค่าคอนฟิกแบบจำลองข้อมูล **รูปแบบการชำระเงิน 1099**
3. บนแท็บด่วน **ส่วนประกอบการตั้งค่าคอนฟิก** ให้เลือกลิงก์ **สำหรับการนำเข้าธุรกรรมด้วยตนเอง 1099**
4. บนหน้า **การแมปรูปแบบกับแหล่งข้อมูล** มีการเลือกการแมปรูปแบบ **สำหรับการนำเข้าธุรกรรมด้วยตนเอง 1099** ไว้ล่วงหน้า เลือก **เรียกใช้**
5. บนแท็บ **พารามิเตอร์** ให้เลือก **เรียกดู** ค้นหาและเลือกไฟล์ **1099import-data.xlsx** แล้วเลือก **ตกลง**
6. ในฟิลด์ **ป้อนรหัสใบสำคัญ** ป้อน **V-00001**
7. บนแท็บ **ทำงานในเบื้องหลัง** ให้ตั้งค่าตัวเลือก **การประมวลผลชุดงาน** เป็น **ใช่**

    โปรดสังเกตว่าฟิลด์ **รายละเอียดงาน** ตั้งค่าเป็น **การเรียกใช้การตั้งค่าคอนฟิกการแมปรูปแบบ 'สำหรับการนำเข้าธุรกรรมด้วยตนเอง 1099' เป็น 'รูปแบบการชำระเงิน 1099'** ค่านี้แสดงว่าการดำเนินการของการแมปรูปแบบที่เลือกจะจัดกำหนดการเป็นชุดงานใหม่

    ![การระบุรายละเอียดของการนําเข้าข้อมูลในโหมดชุดงานในกล่องโต้ตอบพารามิเตอร์ของรายงานอิเล็กทรอนิกส์](./media/er-configure-data-import-batch-execution-parameters.png)

8. เลือก **ตกลง** ข้อความแจ้งให้คุณทราบว่าชุดงานใหม่ถูกจัดกำหนดการแล้ว

    ![ข้อความเกี่ยวกับชุดงานที่จัดกำหนดการใหม่ในหน้าการแมปรูปแบบกับแหล่งข้อมูล](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>ตรวจสอบผลการนำเข้าข้อมูลในหน้าชุดงาน

1. ไปยัง **ทั่วไป** \> **การสอบถาม** \> **งานชุดงาน** \> **งานชุดงานของฉัน**
2. บนหน้า **ชุดงาน** ให้กรองรายการของชุดงานเพื่อค้นหาชุดงานที่จัดกำหนดการ แล้วเลือก
3. เลือกลิงก์ **รหัสงาน** เพื่อตรวจสอบรายละเอียดงาน
4. บนแท็บด่วน **ชุดงาน** ให้เลือก **บันทึก**

    ![ปุ่มบันทึกบนหน้าชุดงาน](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. ตรวจสอบรายละเอียดการดำเนินการ

    ![บันทึกการดำเนินการของชุดงานที่จัดกำหนดการบนหน้าชุดงาน](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>เปลี่ยนพารามิเตอร์การนําเข้าข้อมูล

หลังจากที่จัดกำหนดการชุดงานของคุณแล้ว และในขณะที่ยังไม่ได้เรียกใช้ คุณสามารถเปลี่ยนพารามิเตอร์ของการนําเข้าข้อมูลที่จัดกำหนดการแล้วได้

1. ไปยัง **ทั่วไป** \> **การสอบถาม** \> **งานชุดงาน** \> **งานชุดงานของฉัน**
2. บนหน้า **ชุดงาน** ให้กรองรายการของชุดงานเพื่อค้นหาชุดงานที่จัดกำหนดการ แล้วเลือก
3. เลือก **เปลี่ยนแปลงสถานะ**
4. ในกล่องโต้ตอบ **เลือกสถานะใหม่** ให้เลือก **ระงับ** แล้วเลือก **ตกลง**
5. เลือกลิงก์ **รหัสงาน** เพื่อเข้าถึงรายละเอียดงาน
6. บนแท็บด่วน **ชุดงาน** ให้เลือก **พารามิเตอร์**
7. ในกล่องโต้ตอบ **พารามิเตอร์ของรายงานทางอิเล็กทรอนิกส์** ให้ทำตามขั้นตอนเหล่านี้

    1. เลือก **เรียกดู** เพื่อเลือกไฟล์อื่นที่จะนําเข้าข้อมูล
    2. เลือก **ป้อนรหัสใบสำคัญ** เพื่อเปลี่ยนหมายเลขใบสำคัญสำหรับการนำเข้าธุรกรรมผู้จัดจำหน่าย

        ![การเปลี่ยนพารามิเตอร์ของการนําเข้าข้อมูลสำหรับชุดงานที่จัดกำหนดการแล้วในกล่องโต้ตอบพารามิเตอร์ของรายงานอิเล็กทรอนิกส์](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. เลือก **ตกลง**

8. ตรวจสอบให้แน่ใจว่าชุดงานยังคงถูกเลือกอยู่ แล้วเลือก **เปลี่ยนสถานะ** อีกครั้ง
9. ในกล่องโต้ตอบ **เลือกสถานะใหม่** ให้เลือก **กำลังรอ** แล้วเลือก **ตกลง**

## <a name="review-the-data-import-results-on-the-er-source-page"></a>ตรวจสอบผลการนำเข้าข้อมูลในหน้าต้นทาง ER

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **แหล่งที่มาการรายงานทางอิเล็กทรอนิกส์**
2. เลือกเรกคอร์ด **สำหรับการนำเข้าธุรกรรมของผู้จัดจำหน่าย (Excel)** ที่สร้างขึ้นโดยอัตโนมัติในระหว่างการนําเข้าข้อมูล

    ![เรกคอร์ดสำหรับการตั้งค่าคอนฟิกสำหรับการนำเข้าธุรกรรมของผู้จัดจำหน่าย (Excel) ในหน้าต้นทางการรายงานทางอิเล็กทรอนิกส์](./media/er-configure-data-import-batch-files-source-1.png)

3. เลือก **สถานะไฟล์สำหรับต้นทาง**
4. บนแท็บด่วน **ไฟล์** และ **บันทึกต้นทางสำหรับรูปแบบการนำเข้า** ให้ตรวจสอบรายละเอียดการนำเข้า
5. บนแท็บด่วน **ไฟล์** ให้เลือกเรกคอร์ด โปรดสังเกตว่าไฟล์ที่นําเข้าแนบอยู่กับเรกคอร์ดนี้

    ![ไฟล์ที่นําเข้าที่แนบกับเรกคอร์ดในสถานะไฟล์สำหรับหน้าต้นทาง](./media/er-configure-data-import-batch-files-source-2.png)

6. เลือก **สิ่งที่แนบ** เพื่อตรวจสอบไฟล์ที่นำเข้า

    ![ไฟล์ที่นําเข้าในหน้ามุมมองเอกสาร](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > เมื่อต้องการเก็บสิ่งที่แนบเหล่านี้ กรอบงาน ER จะใช้ชนิดเอกสารที่ [ตั้งค่า](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) สำหรับบริษัทปัจจุบันในฟิลด์ **อื่นๆ** ของพารามิเตอร์ ER

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>ตรวจสอบผลลัพธ์การนําเข้าข้อมูลในหน้าการชำระเงินให้แก่ผู้จัดจำหน่ายสำหรับ 1099

1. ไปที่ **บัญชีเจ้าหนี้** \> **งานประจำงวด** \> **ภาษี 1099** \> **การชำระเงินให้แก่ผู้จัดจำหน่ายสำหรับ 1099s**
2. ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่ **12/31/2017** (31 ธันวาคม 2017)
3. เลือก **ธุรกรรม 1099 แบบกำหนดเอง**

    ![ธุรกรรมผู้จัดจำหน่ายที่นําเข้าในหน้าธุรกรรมภาษี 1099](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
