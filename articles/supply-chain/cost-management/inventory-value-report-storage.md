---
title: รายงานมูลค่าสินค้าคงคลัง
description: บทความนี้อธิบายวิธีการตั้งค่า สร้าง และใช้รายงานมูลค่าสินค้าคงคลัง รายงานเหล่านี้จะให้รายละเอียดเกี่ยวกับปริมาณและยอดเงินทางกายภาพและทางการเงินของสินค้าคงคลังของคุณ
author: JennySong-SH
ms.date: 11/28/2022
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup, InventValueExecutionHistory, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6b21f6a7856526863914aac73d50e5c3a70605e8
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806418"
---
# <a name="inventory-value-reports"></a>รายงานมูลค่าสินค้าคงคลัง

[!include [banner](../includes/banner.md)]

รายงานมูลค่าสินค้าคงคลังจะให้รายละเอียดเกี่ยวกับปริมาณและยอดเงินทางกายภาพและทางการเงินของสินค้าคงคลังของคุณ คุณสามารถดูรายงานในวิธีต่างๆ ต่อไปนี้ ตัวอย่างเช่น คุณสามารถแสดงยอดรวมหรือธุรกรรม หรือกรองตามสินค้าหรือช่วงเวลา คุณสามารถดูมูลค่าต้นทุนของสินค้าที่ขาย (COGS) หรือมูลค่าของงานระหว่างผลิต (WIP) และตั้งค่าตัวเลือกอื่นๆ ได้

รายงานมูลค่าสินค้าคงคลังช่วยให้คุณสามารถปฏิบัติงานต่อไปนี้:

- ทำการกระทบยอดระหว่างบัญชีแยกประเภททั่วไปและสินค้าคงคลัง
- ปรึกษาปริมาณคงคลังคงเหลือและมูลค่าในช่วงระยะเวลาหนึ่งๆ
- สร้างการตั้งค่าคอนฟิกรายงานที่ปรับให้เหมาะกับวัตถุประสงค์เฉพาะหนึ่งๆ
- บันทึกการตั้งค่าคอนฟิกรายงานเพื่อให้สามารถใช้การตั้งค่าคอนฟิกเหล่านั้นได้หลายครั้ง
- เพิ่มช่วงที่จะกรองข้อมูลเมื่อคุณรันรายงาน

## <a name="types-of-inventory-value-report"></a>ชนิดของรายงานมูลค่าสินค้าคงคลัง

รายงานมูลค่าสินค้าคงคลังมีอยู่สองชนิด ได้แก่ **มูลค่าสินค้าคงคลัง** (รายงานมาตรฐาน) และ **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**

### <a name="standard-inventory-value-report"></a>รายงานมูลค่าสินค้าคงคลังมาตรฐาน

รายงาน **มูลค่าสินค้าคงคลัง** มาตรฐานเป็นรายงานแบบง่ายที่ช่วยให้คุณสามารถเลือกข้อมูลที่รวมไว้ จากนั้นแสดงข้อมูลดังกล่าวบนหน้าจอ ไม่ได้บันทึกผลลัพธ์ นอกจากนี้ ยังไม่มีคุณลักษณะการโต้ตอบเกี่ยวกับการกรอง การดูรายละเอียดแนวลึก การเลือกดู หรือการส่งออก เนื่องจากเหตุผลดังกล่าว ขอแนะนำว่าคุณควรใช้รายงาน **ที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง** แทนในกรณีส่วนใหญ่

### <a name="inventory-value-report-storage-report"></a>รายงานที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง

รายงาน **ที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง** ให้ผลลัพธ์เป็นหน้าแบบโต้ตอบใน Microsoft Dynamics 365 Supply Chain Management หรือเป็นเอกสารที่ส่งออกในหนึ่งในรูปแบบ

เมื่อคุณดูรายงานในเบราเซอร์ของคุณ คอลัมน์และยอดดุลรวมจะมีการปรับปรุงแบบไดนามิก โดยขึ้นอยู่กับโครงร่างที่คุณตั้งค่าคอนฟิก คุณสามารถเรียงลำดับผลลัพธ์ กรองข้อมูล ดูรายละเอียดแนวลึกลงในข้อมูล และอื่นๆ

ผลลัพธ์ของรายงานจะถูกจัดเก็บไว้ในเอนทิตี้ข้อมูล **มูลค่าของสินค้าคงคลัง** ดังนั้น คุณจึงสามารถกรองและส่งออกผลลัพธ์ไปยังรูปแบบต่างๆ เช่น ค่าที่แบ่งด้วยเครื่องหมายจุลภาค (CSV) หรือรูปแบบ Microsoft Excel

รายงาน **ที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง** จะมีประโยชน์ เมื่อผลลัพธ์มีหลายรายการ ตัวอย่างเช่น คุณมีสินค้า 50,000 รายการและมีการสร้างร้านค้า 300 แห่ง เป็นคลังสินค้า ในกรณีนี้ ถ้าคุณร้องขอยอดดุลสิ้นงวดของสินค้าคงคลังโดยเรียงตามสินค้า ไซต์ และคลังสินค้า ผลลัพธ์จะประกอบด้วยหลายรายการ

> [!NOTE]
> รายงาน **ที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง** จะไม่มีผลรวมย่อยที่กำหนดไว้ในโครงร่างรายงาน นอกจากนี้ จะไม่มีการรวมยอดดุลบัญชีแยกประเภททั่วไป แม้กระทั่งยอดดุลเหล่านั้นที่จะมีการกำหนดในโครงร่างรายงาน ต้องทำการกระทบยอดกับบัญชีแยกประเภททั่วไปโดยใช้ยอดดุลทดลอง อย่างไรก็ตาม รายงาน **มูลค่าสินค้าคงคลัง** มาตรฐานจะรวมผลรวมย่อยและยอดดุลเหล่านี้ด้วย

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>เปิดหรือปิดคุณลักษณะการจัดเก็บรายงานมูลค่าสินค้าคงคลัง

การใช้คุณลักษณะนี้ ต้องเปิดคุณลักษณะนี้ในระบบของคุณก่อน เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้จะเปิดไว้ ตามค่าเริ่มต้น เริ่มจาก Supply Chain Management เวอร์ชัน 10.0.29 คุณลักษณะนี้เป็นแบบบังคับ และไม่สามารถปิดได้ ถ้าคุณเรียกใช้รุ่นที่เก่ากว่า 10.0.29 ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้ โดยค้นหาคุณลักษณะ *ที่เก็บข้อมูลรายงานมูลค่าสินค้าคงคลัง* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>กําหนดการตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลัง

ใช้หน้า **รายงานมูลค่าสินค้าคงคลัง** เพื่อตั้งค่าเนื้อหาที่รวมอยู่ในรายงานมูลค่าสินค้าคงคลังชนิดต่างๆ คุณสามารถกําหนดชนิดรายงานได้หลายชนิด ในแต่ละครั้งที่คุณสร้างรายงานมูลค่าสินค้าคงคลังชนิดใดชนิดหนึ่ง คุณจะเลือกชนิดรายงาน

1. ไปที่ **การจัดการต้นทุน \> การตั้งค่านโยบายการบัญชีสินค้าคงคลัง \> รายงานมูลค่าสินค้าคงคลัง**
1. ทำตามขั้นตอนเหล่านี้

    - ถ้าต้องการแก้ไขรายงานที่มีอยู่ ให้เลือกในบานหน้าต่างรายการ แล้วจากนั้น เลือก **แก้ไข** ในบานหน้าต่างการดำเนินการ
    - เพื่อสร้างรายงานใหม่: เลือก **สร้าง** บนบานหน้าต่างการดำเนินการ

1. ในส่วนหัวของรายงานใหม่หรือที่เลือก ให้ตั้งค่าฟิลด์ต่อไปนี้:

    - **รหัส** – ป้อนรหัสแบบย่อสำหรับรายงาน ค่านี้ต้องไม่เฉพาะระหว่างการตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลังทั้งหมด ไม่สามารถแก้ไขค่าได้หลังจากที่คุณบันทึกการตั้งค่าคอนฟิกใหม่
    - **ชื่อ** – ป้อนชื่อที่เป็นคำอธิบายสำหรับรายงาน

1. ถ้าคุณจะสร้างการกำหนดค่าคอนฟิกรายงานใหม่ ให้เลือก **บันทึก** ในบานหน้าต่างการดำเนินการเพื่อให้ฟิลด์ที่เหลือพร้อมใช้งาน
1. บน FastTab **ทั่วไป** ตั้งค่าฟิลด์ต่อไปนี้:

    - **ช่วงวันที่** – เลือกช่วงวันที่ที่กําหนดล่วงหน้า คุณสามารถแทนที่ช่วงวันที่นี้เมื่อคุณรันรายงาน
    - **ช่วง** – เลือก *วันที่ลงรายการบัญชี* หรือ *เวลาธุรกรรม* โดยขึ้นอยู่กับวันที่และเวลาที่ควรใช้เมื่อมีการดึงข้อมูลเรกคอร์ดของรายงาน
    - **ชุดของมิติ** – เลือกชุดของมิติที่จะรันข้อมูล (มิติจะถูกระบุในบัญชีแยกประเภททั่วไป) ตัวอย่างเช่น คุณอาจรันข้อมูลเป็น *บัญชีหลัก* หรือ *บัญชีหลัก + หน่วยธุรกิจ* ชุดของมิติที่คุณเลือกต้องมีไม่เกินสองมิติ สำหรับข้อมูลเพิ่มเติม ให้ดู [ชุดมิติทางการเงิน](../../finance/general-ledger/financial-dimension-sets.md)

1. บน FastTab **คอลัมน์** ให้ตั้งค่าฟิลด์ต่อไปนี้ ฟิลด์เหล่านี้จะควบคุมคอลัมน์ที่รวมรายงานของคุณอยู่และชนิดของข้อมูลที่มีคอลัมน์เหล่านั้น

    - **สินค้าคงคลัง** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงมูลค่าสินค้าคงคลัง คุณจะสามารถกระทบยอดค่าเหล่านั้นกับยอดดุลบัญชีแยกประเภททั่วไปได้
    - **WIP** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงมูลค่า WIP คุณจะสามารถกระทบยอดค่าเหล่านั้นกับยอดดุลบัญชี WIP ในบัญชีแยกประเภททั่วไปได้ เมื่อคุณตั้งค่าตัวเลือกนี้เป็น *ใช่* รายงานจะแสดงเฉพาะปริมาณทางกายภาพและยอดสินค้าคงคลังที่มีสถานะ WIP เท่านั้น ใบสั่งผลิตที่มีสถานะ WIP จะถูกเลือกหรือถูกรายงานว่าดำเนินการสำเร็จแล้ว แต่ยังไม่สิ้นสุด
    - **COGS ที่รอการตัดบัญชี** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงปริมาณทางกายภาพและยอดสินค้าคงคลังใน COGS ที่รอการตัดบัญชี COGS ที่รอการตัดบัญชีจะถูกแสดงโดยการใช้ปริมาณและยอดเงินตามจริง เนื่องจากจะออฟเซ็ตปริมาณและยอดเงินในบันทึกการจัดส่ง
    - **COGS** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงปริมาณทางการเงินและยอดสินค้าคงคลังใน COGS COGS จะถูกแสดงโดยการใช้ปริมาณและยอดเงินทางการเงิน เนื่องจากจะออฟเซ็ตปริมาณตามใบแจ้งหนี้
    - **กําไรขาดทุน** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงยอดเงินทางการเงินที่ลงรายการบัญชีในบัญชีกําไรขาดทุนของสินค้าคงคลัง
    - **พิมพ์มูลค่าบัญชีสะสมเพื่อการเปรียบเทียบ** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงยอดดุลบัญชีแยกประเภททั่วไป ด้วยวิธีนี้ คุณไม่จำเป็นต้องตรวจสอบยอดดุลของบันทึก ตัวเลือกนี้จะใช้ได้กับรายงาน **มูลค่าสินค้าคงคลัง** มาตรฐานเท่านั้น ไม่ใช่กับรายงาน **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง** หลังจากที่คุณตั้งค่าตัวเลือกนี้เป็น *ใช่* คุณต้องใช้ฟิลด์ต่อไปนี้เพื่อระบุบัญชีแยกประเภททั่วไปแต่ละบัญชีที่คุณต้องการแสดงรายการ ทั้งนี้ขึ้นอยู่กับตัวเลือก **ตําแหน่งทางการเงิน** ที่คุณเปิดใช้งาน

        > [!NOTE]
        > ถ้าคุณเลือกบัญชี *ผลรวม* ในฟิลด์ใดๆ เหล่านี้ ทั้งยอดเงินของบัญชีสินค้าคงคลังแต่ละบัญชีที่รวมอยู่ในบัญชี ผลรวมและยอดเงินของบัญชีผลรวมจะแสดงขึ้น

        - **บัญชีสินค้าคงคลัง** – ระบุบัญชีแยกประเภททั่วไปเพื่อจะแสดงข้อมูลสินค้าคงคลัง (ต้อตั้งค่าตัวเลือก **สินค้าคงคลัง** และตัวเลือก **พิมพ์มูลค่าบัญชีสะสมเพื่อการเปรียบเทียบ** เป็น *ใช่*)
        - **บัญชี WIP** – ระบุบัญชีแยกประเภททั่วไปเพื่อแสดงข้อมูล WIP (ต้องตั้งค่าตัวเลือก **WIP** และตัวเลือก **พิมพ์มูลค่าบัญชีสะสมเพื่อการเปรียบเทียบ** เป็น *ใช่*)
        - **บัญชี COGS ที่รอการตัดบัญชี** – ระบุบัญชีแยกประเภททั่วไปเพื่อแสดงข้อมูล COGS ที่รอการตัดบัญชี (ต้องตั้งค่าตัวเลือก **COGS ที่รอการตัดบัญชี** และตัวเลือก **พิมพ์มูลค่าบัญชีสะสมเพื่อการเปรียบเทียบ** เป็น *ใช่*)
        - **บัญชี COGS** – ระบุบัญชีแยกประเภททั่วไปเพื่อแสดงข้อมูล COGS (ต้องตั้งค่าตัวเลือก **COGS** และตัวเลือก **พิมพ์มูลค่าบัญชีสะสมเพื่อการเปรียบเทียบ** เป็น *ใช่*)

    - **สรุปค่าที่มีอยู่จริงและมูลค่าทางการเงิน** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงปริมาณรวมของสินค้าคงคลังและยอดสินค้าคงคลัง (ผลรวมของมูลค่า สินค้าคงคลังทางกายภาพและทางการเงิน) ถ้าตั้งค่าตัวเลือกนี้เป็น *ไม่* รายงานจะแสดงทั้งมูลค่าสินค้าคงคลังทางกายภาพและทางการเงิน
    - **รวมรายการที่ไม่ได้ลงรายการบัญชีในบัญชีแยกประเภท** ให้ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงธุรกรรมที่ไม่เคยลงในรายการบัญชีแยกประเภททั่วไป ธุรกรรมในชนิดสินค้าต่อไปนี้อาจไม่ได้บันทึกลงในรายการบัญชีแยกประเภททั่วไป

        - สินค้าที่ได้รับและยังไม่ได้ออกใบแจ้งหนี้จะถูกล้างด้วยกลุ่มแบบจำลองมูลค่าสินค้าที่เกี่ยวข้อง ขณะที่ตัวเลือก **ลงรายการบัญชีสินค้าคงคลังทางกายภาพ**
        - สินค้าที่ได้รับและยังไม่ได้ออกใบแจ้งหนี้จะถูกล้าง เมื่อตัวเลือก **ลงรายการบัญชีใบรับสินค้าในบัญชีแยกประเภท** อยู่บน FastTab **ใบรับสินค้า** บนแท็บ **ทั่วไป** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้** (**บัญชีเจ้าหนี้ \> ตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**)

    - **การคํานวณต้นทุนเฉลี่ยต่อหน่วย** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงต้นทุนเฉลี่ยต่อหน่วย ต้นทุนเฉลี่ยต่อหน่วยคือจำนวนเงินรวมหารด้วยปริมาณรวม
    - **ปริมาณและมูลค่ารวม** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงคอลัมน์ที่แสดงปริมาณรวมของสินค้าคงคลังที่มีอยู่จริง (และปริมาณทางการเงิน) และผลรวมของมูลค่าสินค้าคงคลังที่มีอยู่จริง (และมูลค่าทางการเงิน) คุณสามารถกำหนดตัวเลือกนี้เป็น *ใช่* เมื่อมีการตั้งค่าตัวเลือก **สรุปมูลค่าทางกายภาพและทางการเงิน** เป็น *ไม่*
    - **มิติของสินค้าคงคลัง** – ในกริดนี้ ให้เลือกกล่องกาเครื่องหมาย **มุมมอง** ของแต่ละมิติที่คุณต้องการให้แสดงในรายงาน เฉพาะมิติที่ตัวเลือก **สินค้าคงคลังทางการเงิน** ที่เปิดใช้งานเท่านั้นที่จะแสดงมูลค่าในรายงาน มิติอื่นจะแสดงเฉพาะคอลัมน์ที่ว่างเปล่าเท่านั้น สำหรับมิติที่คุณเลือกจะให้แสดง คุณสามารถเลือกกล่องกาเครื่องหมาย **ผลรวม** เพื่อรวมผลรวมด้วย
    - **รหัสทรัพยากร** – ตั้งค่าตัวเลือก **มุมมอง** เป็น *ใช่* เพื่อแสดงคอลัมน์ที่ระบุสินค้าของแต่ละแถว ตั้งค่าตัวเลือก **ผลรวม** เป็น *ใช่* เพื่อรวมผลรวมด้วย คอลัมน์จะแสดงข้อมูลชนิดใดชนิดหนึ่งต่อไปนี้ โดยขึ้นอยู่กับชนิดของสินค้าที่แสดงในแต่ละแถว

        - **วัสดุ** – คอลัมน์ที่แสดงค่าฟิลด์ `ItemID` ของเรกคอร์ดวัสดุที่เกี่ยวข้อง
        - **แรงงาน** – คอลัมน์ที่แสดงค่าฟิลด์ `WorkCenterID` ของเรกคอร์ดแรงงานที่เกี่ยวข้อง
        - **ต้นทุนทางอ้อม** – คอลัมน์ที่แสดงค่าฟิลด์ `CodeID` ของเรกคอร์ดต้นทุนที่เกี่ยวข้อง

        ถ้าตัวเลือก **มุมมอง** มีการตั้งค่าเป็น *ไม่* ทั้งในฟิลด์ **รหัสทรัพยากร** และฟิลด์ **กลุ่มทรัพยากร** คุณจะเห็นเฉพาะมูลค่าสินค้าคงคลังรวมที่ขึ้นอยู่กับมิติสินค้าคงคลังที่คุณเลือกไว้เท่านั้น

    - **กลุ่มทรัพยากร** – ตั้งค่าตัวเลือก **มุมมอง** เป็น *ใช่* เพื่อแสดงคอลัมน์ที่ระบุกลุ่มทรัพยากรของแต่ละแถว ตั้งค่าตัวเลือก **ผลรวม** เป็น *ใช่* เพื่อรวมผลรวมด้วย คอลัมน์จะแสดงข้อมูลชนิดใดชนิดหนึ่งต่อไปนี้ โดยขึ้นอยู่กับชนิดของสินค้าที่แสดงในแต่ละแถว

        - **วัสดุ** – คอลัมน์ที่แสดงค่าฟิลด์ `ItemGroup` ของเรกคอร์ดวัสดุที่เกี่ยวข้อง
        - **แรงงาน** – คอลัมน์ที่แสดงค่าฟิลด์ `WorkcenterGroup` ของเรกคอร์ดแรงงานที่เกี่ยวข้อง
        - **ต้นทุนทางอ้อม** – คอลัมน์ที่แสดงค่าฟิลด์ `CostGroup` ของเรกคอร์ดต้นทุนที่เกี่ยวข้อง มูลค่า `CostGroupType` ต้องเป็น *ทางอ้อม*

        ถ้าตัวเลือก **มุมมอง** มีการตั้งค่าเป็น *ไม่* ทั้งในฟิลด์ **รหัสทรัพยากร** และฟิลด์ **กลุ่มทรัพยากร** คุณจะเห็นเฉพาะมูลค่าสินค้าคงคลังรวมที่ขึ้นอยู่กับมิติสินค้าคงคลังที่คุณเลือกไว้เท่านั้น

1. บน FastTab **แถว** ให้ตั้งค่าฟิลด์ต่อไปนี้ ฟิลด์เหล่านี้จะช่วยให้คุณเพิ่มส่วนย่อยที่เกี่ยวข้องกับ WIP ที่สอดคล้องกันในรายงานหรือลบส่วนย่อยเหล่านั้นออก

    - **วัสดุ** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงข้อมูลเกี่ยวกับวัสดุ *วัสดุ* เป็นชนิดทรัพยากรเริ่มต้น เนื่องจากวัสดุต้องรวมอยู่ในการตั้งค่าคอนฟิกรายงานทั้งหมด เพื่อสร้างผลลัพธ์ที่เชื่อถือได้
    - **แรงงาน** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงต้นทุนแรงงานของ WIP
    - **ต้นทุนทางอ้อม** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงต้นทุนทางอ้อมของ WIP
    - **การเอาท์ซอร์สทางอ้อม** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงต้นทุนการเอาท์ซอร์สทางอ้อมของ WIP ข้อมูลนี้จะมีประโยชน์สำหรับการรับเหมารายย่อย
    - **ระดับรายละเอียด** – เลือกตัวเลือกมุมมองเกี่ยวกับรายงาน

        - *ธุรกรรม* - ดูธุรกรรมที่เกี่ยวข้องทั้งหมดในรายงาน คุณอาจประสบปัญหาด้านประสิทธิภาพเมื่อคุณดูรายงานที่มีธุรกรรมในปริมาณมาก ดังนั้น หากคุณต้องการใช้ตัวเลือกมุมมองนี้ เราขอแนะนำให้คุณใช้รายงาน **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**
        - *ผลรวม* – ดูผลลัพธ์รวม

    - **รวมยอดดุลต้นงวด** – ตั้งค่าตัวเลือกนี้เป็น *ใช่* เพื่อแสดงยอดดุลต้นงวด ตัวเลือกนี้พร้อมใช้งานเฉพาะเมื่อตั้งค่าฟิลด์ **ระดับรายละเอียด** เป็น *ธุรกรรม* เท่านั้น

## <a name="generate-an-inventory-value-report-storage-report"></a>สร้างรายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง

ทำตามขั้นตอนต่อไปนี้เพื่อสร้างและจัดเก็บรายงาน **รายงานการจัดเก็บมูลค่าสินค้าคงคลัง**

1. ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**
1. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในกล่องโต้ตอบ **มูลค่าสินค้าคงคลัง** บน FastTab **พารามิเตอร์** ให้ตั้งค่าฟิลด์ต่อไปนี้

    - **ชื่อ** – ป้อนชื่อเฉพาะสำหรับรายงาน
    - **รหัส** – เลือก [การตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลัง](#report-configuration) ที่จะใช้กับรายงาน การตั้งค่าคอนฟิกจะสร้างตัวเลือกของคอลัมน์และแถวที่จะรวมอยู่ในรายงานของคุณ
    - **ช่วงวันที่** – ใช้ฟิลด์ในส่วนนี้เพื่อกําหนดเรกคอร์ดที่จะรวมในรายงาน เมื่อต้องการกำหนดช่วงวันที่ คุณสามารถเลือกช่วงที่กำหนดไว้ล่วงหน้า (เทียบกับวันที่สร้างรายงาน) ในฟิลด์ **รหัสช่วงวันที่** หรือเลือกวันที่เฉพาะในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**

1. บน FastTab **เรกคอร์ดที่จะรวม** ให้ตั้งค่าตัวกรองข้อมูลและข้อจำกัดเพื่อกำหนดข้อมูลที่จะถูกรวมไว้ในรายงาน เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบการสอบถามมาตรฐาน ซึ่งคุณจะสามารถกําหนดเงื่อนไขการเลือก เงื่อนไขการเรียงลำดับ และการรวม ฟิลด์จะทำงานเช่นเดียวกับทำให้ชนิดการสอบถามอื่นๆ ใน Supply Chain Management ตัวกรองข้อมูลทั้งหมดนี้จะนำไปใช้กับรายการความเคลื่อนไหวของสินค้าคงคลัง แต่ไม่ใช้กับยอดดุลบัญชีแยกประเภททั่วไป โปรดคำนึงถึงพฤติกรรมนี้เมื่อคุณตั้งค่าตัวกรองข้อมูล มิฉะนั้น คุณอาจเห็นความขัดแย้งระหว่างสินค้าคงคลังและบัญชีแยกประเภททั่วไป
1. บน FastTab **รันในเบื้องหลัง** ให้ระบุว่าจะสร้างรายงานอย่างไร เมื่อใด และบ่อยครั้งเพียงใด ฟิลด์จะทำงานเช่นเดียวกับทำให้ชนิด [งานเบื้องหลัง](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) อื่นๆ ใน Supply Chain Management

    > [!NOTE]
    > มีการรันรายงานนี้เสมอโดยเป็นส่วนหนึ่งของชุดงาน

1. เลือก **ตกลง** เพื่อใช้การตั้งค่าของคุณ และปิดกล่องโต้ตอบ

หลังจากชุดงานเสร็จสมบูรณ์ รายงานจะถูกแสดงรายการบนหน้า **การจัดเก็บรายงานมูลค่าสินค้าคงคลัง** คุณอาจต้องรีเฟรชหน้าเพื่อดูรายงาน

> [!IMPORTANT]
> ในการตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลังที่เลือก คุณอาจได้รับยอดดุลต้นงวดที่ไม่ถูกต้อง ถ้าคุณเลือกวันเดียวกันทั้งในฟิลด์ **วันที่เริ่มต้น** และฟิลด์ **วันที่สิ้นสุด** และถ้าคุณตั้งค่าตัวเลือก **รวมยอดดุลต้นงวด** เป็น *ใช่* ด้วย

## <a name="explore-an-inventory-value-report-storage-report"></a>สำรวจรายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง

หลังจากที่คุณสร้างรายงานแล้ว คุณสามารถดูและสำรวจได้ตลอดเวลาโดยทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**
1. เลือกรายงานในรายการ ในหน้าแสดงรายละเอียดของ [การตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลัง](#report-configuration) ที่ใช้ในการสร้างรายงานที่เลือก
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **ดูรายละเอียด** เพื่อแสดงเนื้อหาของรายงาน
1. สำรวจรายงานโดยปฏิบัติตามขั้นตอนใดๆ ต่อไปนี้:

    - เช่นกันกับหน้ามาตรฐานส่วนใหญ่ใน Supply Chain Management คุณสามารถเลือกส่วนหัวของคอลัมน์ใดๆ ได้เกือบทั้งหมดเพื่อเรียงลำดับหรือกรองข้อมูลกริดตามค่าในคอลัมน์นั้น
    - ใช้ฟิลด์ **ตัวกรองข้อมูล** เพื่อกรองรายงานตามค่าใดๆ ในคอลัมน์ใดๆ ที่พร้อมใช้งาน
    - ใช้เมนูมุมมอง (เหนือฟิลด์ **ตัวกรองข้อมูล**) เพื่อบันทึกและโหลดชุดโปรดของตัวเลือกการเรียงลำดับและการกรองข้อมูลของคุณ

## <a name="export-an-inventory-value-report-storage-report"></a><a name="export-stored-report"></a>ส่งออกรายงานการจัดเก็บรายงานมูลค่าสินค้าคงคลัง

รายงานทุกฉบับที่คุณสร้างจะถูกจัดเก็บไว้ในเอนทิตี้ข้อมูล **มูลค่าของสินค้าคงคลัง** คุณสามารถใช้คุณลักษณะการจัดการข้อมูลมาตรฐานของ Supply Chain Management เพื่อส่งออกข้อมูลจากเอนทิตี้นี้ไปยังรูปแบบข้อมูลใดๆ ที่ได้รับการสนับสนุน เช่น รูปแบบ CSV หรือ Excel

ตัวอย่างต่อไปนี้แสดงวิธีการส่งออกรายงาน **รายงานการจัดเก็บมูลค่าของสินค้าคงคลัง**

1. ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการข้อมูล**
1. ในส่วน **นำเข้า/ส่งออก** ให้เลือกไทล์ **ส่งออก**
1. บนหน้า **ส่งออก** ที่ปรากฏขึ้น ให้ตั้งค่างานการส่งออก อันดับแรกให้ป้อนชื่อกลุ่มสำหรับงาน
1. ในส่วน **เอนทิตี้ที่เลือก** ให้เลือก **เพิ่มเอนทิตี้**
1. ในกล่องโต้ตอบที่ปรากฏขึ้น ตั้งค่าฟิลด์ต่อไปนี้:

    - **ชื่อเอนทิตี้** – เลือก *มูลค่าของสินค้าคงคลัง*
    - **รูปแบบข้อมูลเป้าหมาย** – เลือกรูปแบบที่จะส่งออกข้อมูลไป

1. เลือก **เพิ่ม** เพื่อเพิ่มแถวใหม่ แล้วเลือก **ปิด** เพื่อปิดกล่องโต้ตอบ
1. โดยปกติ คุณจะส่งออกรายงานครั้งละหนึ่งฉบับ เมื่อต้องการส่งออกรายงานเดียว ให้ตั้งค่าตัวกรองสำหรับแถวที่คุณเพิ่งเพิ่มลงในกล่องโต้ตอบ **การสอบถาม** ด้วยวิธีนี้ คุณสามารถกำหนดรายงานจากเอนทิตี้ **มูลค่าของสินค้าคงคลัง** ที่จะรวมไว้ในการส่งออกของคุณได้ ปฏิบัติตามขั้นตอนต่อไปนี้ในการตั้งค่าตัวเลือกตัวกรองต่อไปนี้เพื่อส่งออกรายงานฉบับเดียว:

    1. บนแท็บ **ช่วง** ให้เลือก **เพิ่ม** เพื่อเพิ่มแถว
    2. ตั้งค่าฟิลด์ **ตาราง** เป็น *มูลค่าของสินค้าคงคลัง*
    3. ตั้งค่าฟิลด์ **ตารางสืบทอด** เป็น *มูลค่าของสินค้าคงคลัง*
    4. ตั้งค่าฟิลด์ **ฟิลด์** เป็นฟิลด์ที่คุณต้องการกรองข้อมูล โดยปกติ คุณจะใช้ฟิลด์ **ชื่อการดำเนินการ** และ/หรือฟิลด์ **เวลาที่ใช้ในการดำเนินการ**
    5. ตั้งค่าฟิลด์ **เงื่อนไข** เป็นค่าที่คุณต้องการค้นหาในฟิลด์ที่เลือก (ถ้าคุณเลือกฟิลด์ **ชื่อการดำเนินการ** ในขั้นตอนก่อนหน้านี้ ค่านี้จะเป็นชื่อของรายงาน ถ้าคุณเลือกฟิลด์ **เวลาที่ใช้ในการดำเนินการ** จะเป็นเวลาที่มีการสร้างรายงาน)
    6. เพิ่มแถวเพิ่มเติมไปยังแท็บ **ช่วง** ตามที่คุณต้องการ จนกว่าคุณจะระบุรายงานที่คุณกำลังค้นหาโดยไม่ซ้ำ

1. เลือก **ตกลง** เพื่อบันทึกการตั้งค่าของคุณ และปิดกล่องโต้ตอบ
1. เลือก **บันทึก** เพื่อบันทึกการตั้งค่าการส่งออกของคุณ
1. บนแท็บ **ตัวเลือกการส่งออก** และเลือก **ส่งออกเดี๋ยวนี้** เพื่อสร้างไฟล์การส่งออก
1. บนหน้า **สรุปการดำเนินการ** ที่ปรากฏขึ้น คุณสามารถดูสถานะของงานการส่งออกของคุณและรายการของเอนทิตี้ที่มีการส่งออก ในส่วน **สถานะการประมวลผลเอนทิตี้** เลือกเอนทิตี้ **มูลค่าของสินค้าคงคลัง** ในรายการ และจากนั้น เลือก **ดาวน์โหลดไฟล์** เพื่อดาวน์โหลดข้อมูลที่ถูกส่งออกจากเอนทิตี้นั้น

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้การจัดการข้อมูลเพื่อส่งออกข้อมูล โปรดดู [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)

## <a name="delete-stored-inventory-value-reports"></a>ลบรายงานมูลค่าสินค้าคงคลังที่จัดเก็บ

เมื่อจํานวนรายงานมูลค่าสินค้าคงคลังที่จัดเก็บเพิ่มขึ้น รายงานอาจเริ่มใช้พื้นที่ว่างในฐานข้อมูลของคุณในที่สุด สถานการณ์นี้สามารถส่งผลกระทบต่อประสิทธิภาพของระบบ และทําให้เกิดต้นทุนการจัดเก็บข้อมูลที่สูงกว่า ดังนั้นคุณจึงอาจต้องล้างข้อมูลรายงานเป็นครั้งคราว โดยการลบรายงานที่เก่ากว่า

> [!IMPORTANT]
> ก่อนที่คุณจะลบรายงานค่าสินค้าคงคลังใดๆ ที่สร้างไว้ก่อนหน้านี้ เราขอแนะนาเป็นอย่างยิ่งว่าคุณควร [ส่งออกรายงาน](#export-stored-report) และจัดเก็บรายงานดังกล่าวภายนอกก่อน เนื่องจากคุณอาจไม่สามารถสร้างรายงานใหม่ได้อีกในภายหลัง มีข้อจํากัดนี้เนื่องจากเมื่อคุณสร้างรายงานมูลค่าสินค้าคงคลัง ระบบจะทำงานย้อนหลังจากวันนี้ และประมวลผลเรกคอร์ดรายการความเคลื่อนไหวของสินค้าคงคลังแต่ละเรกคอร์ด โดยกลับรายการใบสั่งเมื่อเข้าสู่กระบวนการดังกล่าว ถ้าคุณพยายามดูย้อนกลับไปมากเกินเมื่อคุณสร้างรายงาน ปริมาณธุรกรรมที่จะประมวลผลในที่สุดแล้วที่ระบบจะหมดเวลาก่อนที่จะสามารถสร้างรายงานได้เสร็จสิ้น ระยะห่างไปยังอดีตที่คุณสามารถสร้างรายงานใหม่จะขึ้นอยู่กับจํานวนรายการความเคลื่อนไหวของสินค้าคงคลังที่คุณมีในระบบของคุณในช่วงเวลาที่เกี่ยวข้อง

### <a name="delete-one-report-at-a-time"></a>การลบรายงานครั้งละหนึ่งรายการ

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อลบรายงานที่จัดเก็บครั้งละหนึ่งรายการ

1. [ส่งออกรายงาน](#export-stored-report) ที่คุณวางแผนจะลบ และจัดเก็บลงในที่ตั้งภายนอกเพื่อใช้อ้างอิงในอนาคต
1. ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> การจัดเก็บรายงานมูลค่าสินค้าคงคลัง**
1. ในบานหน้าต่างรายการ ให้เลือกรายงานที่จะลบ
1. บนบานหน้าต่างการดำเนินการ ให้เลือก **ลบ**
1. ข้อความเตือนจะเตือนคุณให้กลับค่ารายงานที่สร้างขึ้น เลือก **ใช่** หากคุณพร้อมที่จะดำเนินการลบ

### <a name="delete-several-reports-at-the-same-time"></a>ลบหลายรายงานพร้อมกัน

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อลบรายงานที่จัดเก็บหลายรายการพร้อมกัน

1. [ส่งออกรายงานทั้งหมด](#export-stored-report) ที่คุณวางแผนจะลบ และจัดเก็บลงในที่ตั้งภายนอกเพื่อใช้อ้างอิงในอนาคต
1. ไปที่ **การจัดการต้นทุน \> การบัญชีสินค้าคงคลัง \> ล้าง \> การล้างข้อมูลรายงานมูลค่าสินค้าคงคลัง**
1. ในกล่องโต้ตอบ **การล้างข้อมูลรายงานมูลค่าสินค้าคงคลัง** ในฟิลด์ **ลบรายงานมูลค่าสินค้าคงคลังที่ดำเนินการก่อนหน้านี้** ให้เลือกวันที่ที่ควรลบรายงานมูลค่าสินค้าคงคลังทั้งหมดก่อนหน้านั้น
1. บนแท็บด่วน **เรกคอร์ดที่จะรวม** คุณสามารถตั้งค่าเงือนไขการกรองเพิ่มเติม เพื่อจํากัดชุดของรายงานที่จะถูกลบ เลือก **ตัวกรอง** เพื่อเปิดตัวแก้ไขการสอบถามมาตรฐาน ซึ่งคุณจะสามารถกําหนดคุณสมบัติของรายงานที่จะถูกลบ
1. บนแท็บด่วน **รันในเบื้องหลัง** คุณสามารถระบุ อย่างไร เมื่อใด และบ่อยครั้งเพียงใด ที่รายงานควรจะถูกลบ ฟิลด์จะทำงานเช่นเดียวกับทำให้ชนิด [งานเบื้องหลัง](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) อื่นๆ ใน Supply Chain Management อย่างไรก็ตาม โดยทั่วไปคุณจะรันงานนี้ด้วยตนเองทุกครั้งที่ต้องการ
1. เลือก **ตกลง** เพื่อลบรายงานที่ระบุ

## <a name="generate-a-standard-inventory-value-report"></a>สร้างรายงานการจัดเก็บมูลค่าสินค้าคงคลังมาตรฐาน

ใช้ขั้นตอนต่อไปนี้สร้างรายงาน **มูลค่าสินค้าคงคลัง** มาตรฐาน

1. ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> การบัญชีสินค้าคงคลัง - รายงานสถาน \> มูลค่าสินค้าคงคลัง**
1. ในกล่องโต้ตอบ **รายงานมูลค่าสินค้าคงคลัง** บน FastTab **พารามิเตอร์** ให้ตั้งค่าฟิลด์ต่อไปนี้

    - **ชื่อ** – ป้อนชื่อเฉพาะสำหรับรายงาน
    - **รหัส** – เลือก [การตั้งค่าคอนฟิกรายงานมูลค่าสินค้าคงคลัง](#report-configuration) ที่จะใช้กับรายงาน การตั้งค่าคอนฟิกจะสร้างตัวเลือกของคอลัมน์และแถวที่จะรวมอยู่ในรายงานของคุณ
    - **ช่วงวันที่** – ใช้ฟิลด์ในส่วนนี้เพื่อกําหนดเรกคอร์ดที่จะรวมในรายงาน เมื่อต้องการกำหนดช่วงวันที่ คุณสามารถเลือกช่วงที่กำหนดไว้ล่วงหน้า (เทียบกับวันที่สร้างรายงาน) ในฟิลด์ **รหัสช่วงวันที่** หรือเลือกวันที่เฉพาะในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด**

1. บน FastTab **เรกคอร์ดที่จะรวม** ให้ตั้งค่าตัวกรองข้อมูลและข้อจำกัดเพื่อกำหนดข้อมูลที่จะถูกรวมไว้ในรายงาน เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบการสอบถามมาตรฐาน ซึ่งคุณจะสามารถกําหนดเงื่อนไขการเลือก เงื่อนไขการเรียงลำดับ และการรวม ฟิลด์จะทำงานเช่นเดียวกับทำให้ชนิดการสอบถามอื่นๆ ใน Supply Chain Management
1. บน FastTab **รันในเบื้องหลัง** ให้ระบุว่าจะสร้างรายงานอย่างไร เมื่อใด และบ่อยครั้งเพียงใด ฟิลด์จะทำงานเช่นเดียวกับทำให้ชนิด [งานเบื้องหลัง](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) อื่นๆ ใน Supply Chain Management
1. เลือก **ตกลง** เพื่อใช้การตั้งค่าของคุณ และปิดกล่องโต้ตอบ รายงานที่ปรากฎ

## <a name="reading-inventory-value-reports"></a>การอ่านรายงานมูลค่าสินค้าคงคลัง

ส่วนนี้จะแสดงแนวทางบางอย่างเกี่ยวกับวิธีการอ่านและทำความเข้าใจรายงานมูลค่าสินค้าคงคลัง

Supply Chain Management จะสนับสนุนแนวคิดที่สําคัญสองแนวคิดต่อไปนี้ที่เกี่ยวข้องกับสถานะสินค้าคงคลัง

- **การอัปเดตทางการเงิน** – แนวคิดนี้บ่งชี้ว่าได้มีการออกใบแจ้งหนี้ธุรกรรมของสินค้าคงคลังแล้ว ใบสั่งผลิตจะบ่งชี้ถึงจุดสิ้นสุดของใบสั่งผลิต
- **การอัปเดตจริง** – แนวคิดนี้บ่งชี้ว่าธุรกรรมของสินค้าคงคลังยังไม่ได้ออกใบแจ้งหนี้ แต่ได้รับหรือจัดส่งสินค้าแล้ว ในใบสั่งผลิต จะบ่งชี้ว่ามีการเบิกวัสดุแล้ว หรือมีการรายงานว่าการดำเนินงานตามใบสั่งผลิตเสร็จสิ้นแล้ว

เมื่อคุณเข้าใจแนวคิดทั้งสองนี้ จะสามารถเข้าใจคอลัมน์ต่อไปนี้ในการแสดงผลของรายงานได้ง่ายขึ้น

- **สินค้าคงคลัง: ปริมาณทางการเงิน** - ปริมาณที่มีการอัปเดตทางการเงิน
- **สินค้าคงคลัง: มูลค่าทางการเงิน** - มูลค่าทางการเงินของสินค้าคงคลังสำหรับปริมาณที่มีการอัปเดตทางการเงิน
- **สินค้าคงคลัง: ปริมาณทางกายภาพที่ที่ลงรายการบัญชี** - ปริมาณที่มีการอัปเดตทางกายภาพ
- **สินค้าคงคลัง: จำนวนทางกายภาพที่ลงรายการบัญชี** - มูลค่าจำนวนของสินค้าคงคลังสำหรับปริมาณที่มีการอัปเดตทางกายภาพ
- **สินค้าคงคลัง: ปริมาณทางกายภาพที่ไม่ได้ลงรายการบัญชี** – ปริมาณที่มีธุรกรรมของสินค้าคงคลังแต่ยังไม่ได้ลงรายการบัญชีที่บัญชีแยกประเภททั่วไป ตัวอย่างเช่น คุณมีกลุ่มแบบจำลองสินค้าที่ตัวเลือก **ลงรายการบัญชีสินค้าคงคลังที่มีอยู่จริง** และ **ลงรายการบัญชีสินค้าคงคลังทางการเงิน** ถูกล้างออก และคุณมีสินค้าที่เชื่อมโยงกับกลุ่มนั้น จากนั้นคุณสร้างใบสั่งซื้อ รับใบสั่งซื้อ และออกใบแจ้งหนี้ ณ จุดนี้ ถ้าคุณทบทวนรายงานมูลค่าสินค้าคงคลังของสินค้า คุณจะเห็นว่าปริมาณและมูลค่าบนใบสั่งซื้อจะแสดงอยู่ในคอลัมน์ **Inventory: Physical Quantity Not Posted** และ **Inventory: Physical Amount Not Posted**
- **Inventory: Physical Amount Not Posted** – คุณสามารถตั้งค่ารายงานของคุณเพื่อให้แสดงยอดเงินที่ยังไม่ได้ลงรายการบัญชี อย่างไรก็ตาม อย่าใช้ค่านี้ ถ้าคุณจะใช้รายงานในการกระทบยอดสินค้าคงคลัง  มิฉะนั้น ยอดเงินจะไม่ถูกบันทึกในบัญชีแยกประเภททั่วไป
- **Inventory: Quantity** – ปริมาณรวมของปริมาณคอลัมน์ทั้งหมดบนรายงาน
- **Inventory: Amount** – ปริมาณรวมของปริมาณคอลัมน์ทั้งหมดในรายงาน เมื่อคุณกระทบยอดสินค้าคงคลัง อย่าใช้คอลัมน์นี้ถ้ารายงานของคุณรวมคอลัมน์ **Inventory: Physical Amount Not Posted** ในกรณีนี้ คุณต้องแยกยอด **Inventory: Physical Amount Not Posted** ออกจากยอดเงินรวม
- **ต้นทุนเฉลี่ยต่อหน่วย** - จำนวนรวมหารด้วยปริมาณรวม

โดยทั่วไป คุณจะใช้รายงานมูลค่าสินค้าคงคลังเพื่อดูมูลค่าและปริมาณสินค้าคงคลัง อย่างไรก็ตาม บางครั้งรายงานจะไม่แสดงมิติของสินค้าคงคลังที่เกี่ยวข้องทั้งหมด หากคุณไม่เห็นมิติที่คุณคาดไว้ ให้ตรวจสอบความถูกต้องของการตั้งค่าต่อไปนี้

- ตรวจสอบการจัดเก็บสินค้าและติดตามกลุ่มมิติ เฉพาะมิติที่ตัวเลือก **สินค้าคงคลังทางการเงิน** ที่เปิดใช้งานเท่านั้นที่จะแสดงในรายงาน
- ไปที่ **การจัดการต้นทุน \> การตั้งค่านโยบายการบัญชีของสินค้าคงคลัง \> รายงานมูลค่าสินค้าคงคลัง** ให้เลือกการตั้งค่าคอนฟิกของรายงานที่คุณใช้ในการสร้างรายงาน และตรวจสอบให้แน่ใจว่ามิติของสินค้าคงคลังที่จำเป็นได้ถูกเลือกในคอลัมน์ **มุมมอง**

ตัวอย่างเช่น คุณมีสินค้าที่มีหมายเลขสินค้า *A0001* ในกลุ่มมิติการจัดเก็บ เฉพาะไซต์ที่เปิดใช้งานในสินค้าคงคลังทางการเงินเท่านั้น เปิดใช้งานไซต์และคลังสินค้าในสินค้าคงคลังที่มีอยู่จริง ในการติดตามกลุ่มมิติ ให้เปิดใช้งานหมายเลขชุดงานสำหรับสินค้าคงคลังที่มีอยู่จริงแต่ไม่เปิดใช้กับสินค้าคงคลังทางการเงิน จากนั้นให้คุณใช้การตั้งค่าคอนฟิกรายงานที่มีการเลือกไซต์ คลังสินค้า และหมายเลขชุดงานทั้งหมด เมื่อคุณดูรายงาน คุณจะเห็นค่าเฉพาะของไซต์เท่านั้น คอลัมน์ของคลังสินค้าและหมายเลขชุดงานจะว่างเปล่า เมื่อตัวอย่างนี้แสดงขึ้น รายงานมูลค่าสินค้าคงคลังจะสามารถแสดงได้เฉพาะมิติของสินค้าคงคลังที่เปิดใช้งานสำหรับสินค้าคงคลังทางการเงินเท่านั้น

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
