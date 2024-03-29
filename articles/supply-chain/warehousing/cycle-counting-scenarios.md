---
title: ตัวอย่างสถานการณ์การตรวจนับตามรอบ
description: บทความนี้มีชุดสถานการณ์ที่สำรวจคุณลักษณะการตรวจนับตามรอบของ Microsoft Dynamics 365 Supply Chain Management
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 91a18b6deade6d67fce6b90308671910a4196104
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335749"
---
# <a name="cycle-counting-example-scenarios"></a>ตัวอย่างสถานการณ์การตรวจนับตามรอบ

[!include [banner](../includes/banner.md)]

บทความนี้มีชุดสถานการณ์ที่สำรวจคุณลักษณะการตรวจนับตามรอบของ Microsoft Dynamics 365 Supply Chain Management ก่อนอื่นจะอธิบายความต้องการสภาพแวดล้อม Supply Chain Management ที่มีอยู่ของคุณ จากนั้นขั้นตอนนี้จะอธิบายวิธีตั้งค่าคอนฟิกการตรวจนับตามรอบและอธิบายขั้นการตรวจนับตามรอบทั้งหมด เมื่อคุณเสร็จสิ้นแล้ว คุณควรจะมีความเข้าใจที่ดีเกี่ยวกับการตรวจนับตามรอบ รวมถึงการตรวจนับตามรอบที่แนะนำ การตรวจนับตามรอบที่ไม่เปิดเผย การตรวจนับตามรอบทันที บขีดจำกัดการตรวจนับตามรอบ และแผนการตรวจนับตามรอบ

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

### <a name="make-demo-data-available"></a>ทำให้ข้อมูลสาธิตพร้อมใช้งาน

แต่ละสถานการณ์นี้ในค่าและเรกคอร์ดอ้างอิงบทความนี้ที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Supply Chain Management ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณดำเนินการตามสถานการณ์ ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคล (บริษัท) เป็น **USMF** ก่อนที่คุณจะเริ่มต้น

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>เปิดการสนับสนุนสำหรับแอป Warehouse Management บนมือถือ

หากต้องการใช้แอป Warehouse Management บนมือถือ คุณต้องเปิดคุณลักษณะ *การตั้งค่าผู้ใช้ ไอคอน และชื่อขั้นตอนต่างๆ ของคุณลักษณะแอปคลังสินค้าใหม่* ในระบบของคุณ เริ่มจาก Supply Chain Management รุ่น 10.0.25 คุณลักษณะนี้เป็นแบบบังคับและไม่สามารถปิดได้ ถ้าคุณเรียกใช้รุ่นที่เก่ากว่า 10.0.25 ผู้ดูแลระบบสามารถเปิดหรือปิดฟังก์ชันนี้ได้โดยค้นหาคุณลักษณะ *การตั้งค่าผู้ใช้ ไอคอน และชื่อขั้นตอนต่างๆ ของคุณลักษณะแอปคลังสินค้าใหม่* ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>จัดเตรียมข้อมูลสาธิตเกี่ยวกับสถานการณ์

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อยืนยันว่าข้อมูลสาธิตทั้งหมดที่ต้องใช้ในสถานการณ์ดังกล่าวพร้อมใช้งานในบริษัท USMF ในระบบของคุณ สร้างเรกคอร์ดหรือค่าที่ขาดหายไป

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> ผู้ปฏิบัติงาน**
1. ในบานหน้าต่างรายการ ให้เลือก **Julia Funderburk**
1. บนแท็บด่วน **ผู้ใช้** ให้เลือกแถวที่มีค่าต่อไปนี้ ถ้าแถวที่มีอยู่ไม่มีค่าเหล่านี้ ให้สร้างขึ้น

    - **รหัสผู้ใช้:** *61*
    - **ชื่อผู้ใช้:** *WH61*
    - **คลังสินค้าเริ่มต้น:** *61*
    - **ชื่อเมนู:** *หลัก*

1. บนแท็บด่วน **งาน** ให้ตั้งค่าต่อไปนี้ของผู้ใช้ *61* ถ้าไม่ได้ตั้งค่าไว้อยู่แล้ว:

    - **หัวหน้างานตรวจนับตามรอบ:** *ไม่*
    - **ขีดจำกัดเปอร์เซ็นต์สูงสุด:** *0*
    - **ขีดจำกัดปริมาณสูงสุด:** *0*
    - **ขีดจำกัดค่าสูงสุด:** *0*

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> กลุ่มงาน**
1. กลุ่มงานใช้เพื่อแยกงานคลังสินค้า ที่ขึ้นอยู่กับชนิดของงาน (ในกรณีนี้ งานการตรวจนับตามรอบ) ตรวจสอบให้แน่ใจว่าเรกคอร์ดมีการตั้งค่าต่อไปนี้

    - **รหัสกลุ่มงาน:** *CycleCount*
    - **คำอธิบาย:** *การตรวจนับตามรอบ*

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> รายการเมนูบนอุปกรณ์เคลื่อนที่**
1. ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ดที่ชื่อ *การตรวจนับตามรอบ* ถ้าเรกคอร์ดที่มีอยู่ไม่มีชื่อนี้ ให้สร้างขึ้น ยืนยันหรือตั้งค่าต่อไปนี้ให้กับเรกคอร์ด:

    - **ชื่อรายการในเมนู:** *การตรวจนับตามรอบ*
    - **ชื่อ:** *การตรวจนับตามรอบที่แนะนำ*
    - **โหมด:** *งาน*
    - **ใช้งานที่มีอยู่:** *ใช่*
    - **กําหนดโดย:** *สั่งการโดยระบบ* (ค่านี้จะบ่งชี้ว่า Supply Chain Management จะกําหนดรหัสงานการตรวจนับตามรอบให้กับผู้ปฏิบัติงาน)
    - **แสดงสถานะสินค้าคงคลัง:** *ใช่*

1. ในบานหน้าต่างการดำเนินการ เลือก **การตรวจนับตามรอบ**
1. ในกล่องโต้ตอบ **การตรวจนับตามรอบของอุปกรณ์เคลื่อนที่** ให้ยืนยันหรือตั้งค่าต่อไปนี้

    - **แสดงหมายเลขสินค้า:** *ใช่*
    - **แสดงป้ายทะเบียน:** *ใช่*
    - **จำนวนครั้งที่พยายาม:** *1*

1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ
1. ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ดที่ชื่อ *การตรวจนับตามรอบที่ไม่เปิดเผย* ถ้าเรกคอร์ดที่มีอยู่ไม่มีชื่อนี้ ให้สร้างขึ้น ยืนยันหรือตั้งค่าต่อไปนี้ให้กับเรกคอร์ด:

    - **ชื่อรายการในเมนู:** *การตรวจนับตามรอบที่ไม่เปิดเผย*
    - **ชื่อ:** *การตรวจนับตามรอบที่ไม่เปิดเผย*
    - **โหมด:** *งาน*
    - **ใช้งานที่มีอยู่:** *ใช่*
    - **สั่งการโดย:** *การจัดกลุ่มการตรวจนับตามรอบ* (ค่านี้ระบุว่าผู้ปฏิบัติงานสามารถจัดกลุ่มรหัสงานการตรวจนับตามรอบไปยังสถานที่ โซน หรือกลุ่มงานเฉพาะ)

1. ในบานหน้าต่างการดำเนินการ เลือก **การตรวจนับตามรอบ**
1. ในกล่องโต้ตอบ **การตรวจนับตามรอบของอุปกรณ์เคลื่อนที่** ให้ยืนยันหรือตั้งค่าต่อไปนี้

    - **แสดงหมายเลขสินค้า:** *ไม่*
    - **แสดงป้ายทะเบียน:** *ไม่*
    - **จำนวนครั้งที่พยายาม:** *0*

1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ
1. ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ดที่ชื่อ *การตรวจนับตามรอบทันที* ถ้าเรกคอร์ดที่มีอยู่ไม่มีชื่อนี้ ให้สร้างขึ้น ยืนยันหรือตั้งค่าต่อไปนี้ให้กับเรกคอร์ด:

    - **ชื่อรายการในเมนู:** *การตรวจนับตามรอบทันที*
    - **ชื่อ:** *การตรวจนับตามรอบทันที*
    - **โหมด:** *งาน*
    - **ใช้งานที่มีอยู่:** *ไม่*
    - **กระบวนการสร้างงาน:** *การตรวจนับตามรอบทันที* (ค่านี้ระบุว่าผู้ปฏิบัติงานสามารถตรวจนับสินค้าในที่ตั้งคลังสินค้าได้ตลอดเวลา โดยไม่ต้องสร้างงานการตรวจนับตามรอบ หากต้องการดำเนินการตรวจนับตามรอบทันทีในสถานที่ ผู้ปฏิบัติงานป้อนรหัสสถานที่)

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> อุปกรณ์เคลื่อนที่ \> เมนูบนอุปกรณ์เคลื่อนที่**
1. ในบานหน้าต่างรายการ ให้เลือกเรกคอร์ดที่ชื่อ *สินค้าคงคลัง* ถ้าเรกคอร์ดที่มีอยู่ไม่มีชื่อนี้ ให้สร้างขึ้น ยืนยันว่ารายการเมนูการตรวจนับตามรอบต่อไปนี้ปรากฏในคอลัมน์ **โครงสร้างเมนู**:

    - การตรวจนับตามรอบ
    - การตรวจนับตามรอบที่ไม่เปิดเผย
    - การตรวจนับทันที

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**
1. บนแท็บ **การตรวจนับตามรอบ** ให้กำหนดค่าดังต่อไปนี้:

    - **ชนิดการปรับปรุงการตรวจนับตามรอบเริ่มต้น:** *การตรวจนับตามรอบ* (ฟิลด์นี้จะระบุชนิดสมุดรายวันที่ลงรายการบัญชีเมื่อตรวจนับตามรอบ)
    - **รหัสคลาสงานการตรวจนับตามรอบเริ่มต้น:** *CCount* (ฟิลด์นี้จะระบุคลาสงานที่ใช้เพื่อการตรวจนับตามรอบ)
    - **ระดับความสำคัญของงานการตรวจนับตามรอบเริ่มต้น:** *50* (ฟิลด์นี้จะตั้งค่าระดับความสงมากของงานการตรวจนับตามรอบได้โดยสัมพันธ์กับงานชนิดอื่นๆ ในคลังสินค้า คุณสามารถยกระดับความสำคัญของงานการตรวจนับตามรอบได้โดยการป้อนหมายเลขที่ต่ำกว่าหมายเลขของงานชนิดอื่นๆ)

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> ชนิดการปรับปรุง**
1. หน้า **ชนิดการปรับปรุง** ช่วยให้คุณสามารถสร้างรหัสเกี่ยวกับการปรับปรุงที่มีอยู่และการปรับปรุงที่แตกต่างกันซึ่งอาจเกิดขึ้น ยืนยันว่าเรกคอร์ดมีการตั้งค่าต่อไปนี้:

    - **ชนิดการปรับปรุงสินค้าคงคลัง:** *การตรวจนับตามรอบ*
    - **คำอธิบาย:** *การตรวจนับตามรอบ*
    - **ชื่อ:** *ICnt*

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การตั้งค่าคลังสินค้า \> คลังสินค้า**
1. ในบานหน้าต่างรายการ เลือกคลังสินค้า *61* ถ้าเรกคอร์ดที่มีอยู่ไม่มีชื่อนี้ ให้สร้างขึ้น
1. บนแท็บด่วน **คลังสินค้า** ให้กำหนดค่าดังต่อไปนี้:

    - **ใช้กระบวนการการจัดการคลังสินค้า:** *ใช่* (ค่านี้จะเปิดใช้งานคลังสินค้าในกระบวนการ Warehouse Management (WMS))
    - **อนุญาตป้ายทะเบียนย้ายระหว่างการตรวจนับตามรอบ:** *ใช่* (ค่านี้ช่วยให้ผู้ปฏิบัติงานสามารถย้ายป้ายทะเบียนในระหว่างการตรวจนับตามรอบ)

## <a name="scenario-1-guided-cycle-counting"></a>สถานการณ์ที่ 1: การตรวจนับตามรอบที่แนะนำ

ก่อนที่จะเกิดการตรวจนับตามรอบที่แนะนำ คุณต้องสร้างงานบางอย่าง งานนี้จะแนะนำบุคคลที่ได้รับมอบหมายผ่านทางคลังสินค้า จากสถานที่หนึ่งไปยังสถานที่หนึ่ง เพื่อนับรวมการตรวจนับที่ตั้งค่าในงานให้เสร็จสมบูรณ์

### <a name="create-cycle-counting-work-for-scenario-1"></a>สร้างงานการตรวจนับตามรอบสำหรับสถานการณ์ที่ 1

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างงานการตรวจนับตามรอบของสถานที่เก็บสินค้า *01A02R2S2B* (BULK-06) ในคลังสินค้า *61*

1. ไปที่ **การจัดการคลังสินค้า \> การตรวจนับตามรอบ \> งานการตรวจนับตามรอบตามสถานที่เก็บ**
1. ในกล่องโต้ตอบ **สร้างงานการตรวจนับตามรอบตามสถานที่** ให้ตั้งค่าฟิลด์ **รหัสกลุ่มงาน** เป็น *CycleCount*
1. บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรองข้อมูล**
1. ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้ปฏิบัติตามขั้นตอนต่อไปนี้

    - สำหรับแถวที่ตั้งค่าฟิลด์ **ฟิลด์** เป็น *คลังสินค้า* ตั้งค่าฟิลด์ **เงื่อนไข** เป็น *61*
    - สำหรับแถวที่ตั้งค่าฟิลด์ **ฟิลด์** เป็น *สถานที่เก็บ* ตั้งค่าฟิลด์ **เงื่อนไข** เป็น *01A02R2S2B*

1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม
1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **สร้างงานการตรวจนับตามรอบตามสถานที่**

    เมื่อกระบวนการสร้างงานเสร็จสิ้น จะมีข้อความปรากฏขึ้นในศูนย์การดำเนินการ

1. ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**
1. ค้นหางานที่เพิ่งสร้างขึ้นใหม่โดยตั้งค่าตัวกรองในคอลัมน์ **รหัสกลุ่มงาน** เพื่อค้นหาเรกคอร์ดที่มีค่าเป็น *CycleCount*

### <a name="do-cycle-counting-work-for-scenario-1"></a>ทำงานการตรวจนับตามรอบสำหรับสถานการณ์ที่ 1

หลังจากคุณทำงานการตรวจนับตามรอบ คุณทำงานโดยการนับรายการในที่ตั้งคลังสินค้า และจากนั้นใช้อุปกรณ์มือถือเพื่อป้อนผลใน Supply Chain Management ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อใช้งานการตรวจนับตามรอบในแอป Warehouse Management บนมือถือ

1. ลงชื่อเข้าใช้แอป Warehouse Management บนมือถือเป็นผู้ใช้งานที่ได้ตั้งค่าในส่วน [จัดเตรียมข้อมูลสาธิตให้กับสถานการณ์](#prepare-demo-data) ก่อนหน้านี้ในบทความนี้ ตัวอย่างเช่นในบทความนี้ ผู้ใช้ชื่อ *Julia Funderburk* และมีการตั้งค่าไว้เฉพาะคลังสินค้า *61* (ข้อมูลสาธิต USMF ควรช่วยให้คุณสามารถเข้าสู่ระบบในฐานะผู้ใช้งานนี้โดยการป้อน *61* เป็นรหัสผู้ใช้และ *1* เป็นรหัสผ่าน)
1. บนเมนูหลัก ให้เลือก **สินค้าคงคลัง**
1. บนเมนู **สินค้าคงคลัง** ให้เลือก **การตรวจนับตามรอบที่แนะนำ**
1. เลือกฟิลด์ **ปริมาณ** ป้อน *9* โดยใช้แผ่นหมายเลข แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)
1. ระบบคาดหวังให้คุณป้อน 10 รายการสำหรับสินค้า สถานที่ และป้ายทะเบียนนี้ ดังนั้น จึงขอให้คุณตรวจนับอีกครั้ง เลือกฟิลด์ **ปริมาณ** ป้อน *9* อีกครั้งโดยใช้แผ่นหมายเลข แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก) ในความพยายามครั้งที่สอง การตรวจนับของคุณจะถูกยอมรับ

    > [!NOTE]
    > เมื่อระบบตรวจพบความแตกต่างระหว่างปริมาณคงคลังคงเหลือที่คาดไว้และปริมาณที่คุณป้อน ระบบจะขอให้คุณตรวจนับครั้งที่สอง เนื่องจากฟิลด์ **จํานวนครั้งของความพยายาม** ถูกตั้งค่าเป็น *1* สำหรับรายการเมนู **การตรวจนับตามรอบที่แนะนำ** ของอุปกรณ์เคลื่อนที่ คุณได้รับการแนะนำไปยังหมายเลขสินค้าและหมายเลขป้ายทะเบียนเฉพาะ เนื่องจากทั้งตัวเลือก **หมายเลขสินค้าที่แสดง** และตัวเลือก **ป้ายทะเบียนที่แสดง** ถูกตั้งค่าเป็น *ใช่* สำหรับรายการเมนูในอุปกรณ์เคลื่อนที่

1. เลือก **ตกลง** (ปุ่มสัญลักษณ์เครื่องหมายถูก)

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>ตรวจทานผลต่างการตรวจนับตามรอบสำหรับสถานการณ์ที่ 1

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจทานความแตกต่างของการตรวจนับตามรอบ

1. กลับไปยัง Supply Chain Management
1. ไปที่ **การจัดการคลังสินค้า \> งาน \> รายละเอียดงาน**
1. ค้นหาและเลือกงานการตรวจนับตามรอบที่คุณดูก่อนหน้านี้ (ตัวอย่างเช่น ตั้งค่าตัวกรองข้อมูลบนคอลัมน์ **รหัสกลุ่มงาน** เพื่อค้นหาเรกคอร์ดที่มีค่าของ *CycleCount*) โปรดสังเกตว่าขณะนี้ได้ตั้งค่าฟิลด์ **สถานะงานของงาน** ไว้เป็น *ค้างอยู่รอการตรวจทาน*

    > [!NOTE]
    > ให้กับบัญชีผู้ใช้งานที่คุณใช้ในการงานการตรวจนับ ตัวเลือก **หัวหน้างานการตรวจนับตามรอบ** ถูกตั้งค่าเป็น *ไม่* และฟิลด์ **ขีดจํากัดเปอร์เซ็นต์สูงสุด** **ขีดจํากัดปริมาณสูงสุด** และ **ขีดจํากัดค่าสูงสุด** ถูกตั้งค่าทั้งหมดเป็น *0* (ศูนย์) ดังนั้น ผลต่างการตรวจนับทั้งหมดที่รายงานผู้ใช้นี้ต้องได้รับอนุมัติด้วยตนเอง และฟิลด์ **สถานะของงาน** สำหรับงานที่เกี่ยวข้องถูกตั้งค่าเป็น *ค้างอยู่รอการตรวจทาน* หากค่าที่ตรวจนับอยู่ภายในขีดจํากัดความเบี่ยงเบน (ตามที่ระบุในฟิลด์ **ขีดจํากัดเปอร์เซ็นต์สูงสุด** หรือ **ขีดจํากัดปริมาณสูงสุด** ในหน้า **ผู้ใช้งาน**) หรือถ้ามีการตั้งค่าตัวเลือก **หัวหน้างานตรวจนับตามรอบ** เป็น *ใช่* โดยผู้ใช้ ระบบจะปิดงานโดยอัตโนมัติ

1. บนบานหน้าต่างการดำเนินการ บนแท็บ **งาน** เลือก **การตรวจนับตามรอบ**
1. ในบานหน้าต่างการดำเนินการ เลือก **ยอมรับการตรวจนับ**

    มีการลงรายการบัญชีผลต่างโดยใช้สมุดรายวันการตรวจนับมาตรฐาน และมีการสร้างใบสั่งงานใหม่

1. บนหน้า **ธุรกรรมการตรวจนับตามรอบ** ในบานหน้าต่างการดำเนินการ ให้เลือก **งานที่ได้รับมา** เพื่อค้นหางานที่สร้างไว้ให้กับผลต่างที่อนุมัติ

## <a name="scenario-2-blind-cycle-counting"></a>สถานการณ์ที่ 2: การตรวจนับตามรอบที่ไม่เปิดเผย

สถานการณ์นี้ต้องการให้สถานการณ์ดังกล่าว 1 เสร็จสมบูรณ์ในระบบของคุณแล้ว

### <a name="create-cycle-counting-work-for-scenario-2"></a>สร้างงานการตรวจนับตามรอบสำหรับสถานการณ์ที่ 2

ก่อนที่จะเกิดการตรวจนับตามรอบที่ไม่เปิดเผย คุณต้องสร้างงานบางอย่าง ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างงานการตรวจนับตามรอบของสถานที่เก็บสินค้า *01A02R2S2B* (BULK-06) ในคลังสินค้า *61*

1. ไปที่ **การจัดการคลังสินค้า \> การตรวจนับตามรอบ \> งานการตรวจนับตามรอบตามสินค้า**
1. ในกล่องโต้ตอบ **สร้างงานการตรวจนับตามรอบตามสินค้า** ให้ตั้งค่าฟิลด์ **รหัสกลุ่มงาน** เป็น *CycleCount*
1. บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรองข้อมูล**
1. ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** เพิ่มสามแถวที่มีการตั้งค่าต่อไปนี้:

    - แถว 1:

        - **ตาราง:** *สินค้า*
        - **ฟิลด์:** *Iหมายเลขสินค้า*
        - **เกณฑ์:** *L0101*

    - แถว 2:

        - **ตาราง:** *มิติสินค้าคงคลัง*
        - **ฟิลด์:** *คลังสินค้า*
        - **เงื่อนไข:** *61*

    - แถว 3:

        - **ตาราง:** *มิติสินค้าคงคลัง*
        - **ฟิลด์:** *สถานที่ตั้ง*
        - **เกณฑ์:** *01A02R2S2B*

1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม
1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **สร้างงานการตรวจนับตามรอบตามสินค้า**

    เมื่อกระบวนการสร้างงานเสร็จสิ้น คุณจะได้รับข้อความที่ให้ข้อมูล

### <a name="do-cycle-counting-work-for-scenario-2"></a>ทำงานการตรวจนับตามรอบสำหรับสถานการณ์ที่ 2

หลังจากคุณสร้างงานการตรวจนับตามรอบแล้ว ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อใช้งานการตรวจนับตามรอบในแอป Warehouse Management บนมือถือ

1. ลงชื่อเข้าใช้แอป Warehouse Management บนมือถือเป็นผู้ใช้งานที่ได้ตั้งค่าในส่วน [จัดเตรียมข้อมูลสาธิตให้กับสถานการณ์](#prepare-demo-data) ก่อนหน้านี้ในบทความนี้ ตัวอย่างเช่นในบทความนี้ ผู้ใช้ชื่อ *Julia Funderburk* และมีการตั้งค่าไว้เฉพาะคลังสินค้า *61* (ข้อมูลสาธิต USMF ควรช่วยให้คุณสามารถเข้าสู่ระบบในฐานะผู้ใช้งานนี้โดยการป้อน *61* เป็นรหัสผู้ใช้และ *1* เป็นรหัสผ่าน)
1. บนเมนูหลัก ให้เลือก **สินค้าคงคลัง**
1. บนเมนู **สินค้าคงคลัง** ให้เลือก **การตรวจนับตามรอบที่ไม่เปิดเผย**
1. เลือกฟิลด์ **รหัสโซน** ป้อน *BULK06* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)
1. เลือกฟิลด์ **สินค้า** ป้อน *L0101* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)
1. เลือกฟิลด์ **ป้ายทะเบียน** ป้อน *LP\_BULK\_06\_01* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)
1. เลือกฟิลด์ **บริมาณ** ป้อน *10* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)

    > [!NOTE]
    > แม้ว่าระบบตรวจพบความแตกต่างระหว่างปริมาณคงคลังคงเหลือที่คาดไว้และปริมาณที่คุณสแกน ระบบจะไม่ขอให้คุณตรวจนับครั้งที่สอง เนื่องจากฟิลด์ **จํานวนครั้งของความพยายาม** ถูกตั้งค่าเป็น *0* (ศูนย์) สำหรับรายการเมนู **การตรวจนับตามรอบที่ไม่เปิดเผย** ของอุปกรณ์เคลื่อนที่ ระบบขอให้คุณสแกนหมายเลขสินค้าและป้ายทะเบียน เนื่องจากทั้งตัวเลือก **หมายเลขสินค้าที่แสดง** และตัวเลือก **ป้ายทะเบียนที่แสดง** ถูกตั้งค่าเป็น *ไม่* สำหรับรายการเมนูในอุปกรณ์เคลื่อนที่

1. เลือก **ตกลง** (ปุ่มสัญลักษณ์เครื่องหมายถูก)

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>ตรวจทานผลต่างการตรวจนับตามรอบสำหรับสถานการณ์ที่ 2

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจทานความแตกต่างของการตรวจนับตามรอบ

1. กลับไปยัง Supply Chain Management
1. ไปที่ **การจัดการคลังสินค้า \> ทั่วไป \> งาน \> การตรวจทานที่ค้างอยู่ของงานการตรวจนับตามรอบ**
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **งาน** เลือก **การตรวจนับตามรอบ**
1. ในบานหน้าต่างการดำเนินการ เลือก **ปฏิเสธการตรวจนับ**

    เนื่องจากผลต่างการตรวจนับถูกปฏิเสธ จึงมีการปิดงาน

## <a name="scenario-3-spot-cycle-counting"></a>สถานการณ์ที่ 3: การตรวจนับตามรอบทันที

เรกคอร์ดคงเหลือระบุว่ามีปริมาณคงคลังคงเหลือของสินค้า *L0101* ที่สถานที่ *01A02R2S2B* ผู้ปฏิบัติงานคลังสินค้าอยู่ที่สถานที่ *01A02R2S1B* แม้ว่าสถานที่นี้จะว่างเปล่า แต่สถานที่นี้เต็ม ดังนั้น ผู้ปฏิบัติงานคลังสินค้าจะทำการตรวจนับทันทีของสถานที่นี้

### <a name="do-cycle-counting-work-for-scenario-3"></a>ทำงานการตรวจนับตามรอบสำหรับสถานการณ์ที่ 3

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อใช้งานการตรวจนับตามรอบในแอป Warehouse Management บนมือถือ

1. ลงชื่อเข้าใช้แอป Warehouse Management บนมือถือเป็นผู้ใช้งานที่ได้ตั้งค่าในส่วน [จัดเตรียมข้อมูลสาธิตให้กับสถานการณ์](#prepare-demo-data) ก่อนหน้านี้ในบทความนี้ ตัวอย่างเช่นในบทความนี้ ผู้ใช้ชื่อ *Julia Funderburk* และมีการตั้งค่าไว้เฉพาะคลังสินค้า *61* (ข้อมูลสาธิต USMF ควรช่วยให้คุณสามารถเข้าสู่ระบบในฐานะผู้ใช้งานนี้โดยการป้อน *61* เป็นรหัสผู้ใช้และ *1* เป็นรหัสผ่าน)
1. บนเมนูหลัก ให้เลือก **สินค้าคงคลัง**
1. บนเมนู **สินค้าคงคลัง** ให้เลือก **การตรวจนับทันที**
1. เลือกฟิลด์ **สถานที่** ป้อน *01A02R2S1B* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)

    ระบบตรวจพบว่าสถานที่ว่างเปล่าใน Supply Chain Management

1. เลือก **เพิ่มหมายเลขสินค้าหรือสินค้า**
1. เลือกฟิลด์ **สินค้า** ป้อน *L0101* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)
1. เลือกฟิลด์ **ป้ายทะเบียน** ป้อน *LP\_BULK\_06\_01* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)
1. เลือกฟิลด์ **บริมาณ** ป้อน *9* แล้วเลือก **ตกลง** (ปุ่มเครื่องหมายถูก)

    เนื่องจากระบบตรวจพบว่าป้ายทะเบียนที่ระบุพร้อมใช้งานอยู่แล้วที่สถานที่อื่นใน Supply Chain Management ป้ายทะเบียนนั้นจะถูกย้ายไปยังที่ตั้งปัจจุบัน ดังนั้น ระบบจะขอให้คุณยืนยันการเคลื่อนย้าย

1. เลือก **ตกลง** (ปุ่มสัญลักษณ์เครื่องหมายถูก)

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>ตรวจทานผลต่างการตรวจนับตามรอบสำหรับสถานการณ์ที่ 3

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจทานผลลัพธ์ของการตรวจนับ

1. กลับไปยัง Supply Chain Management
1. ไปที่ **การจัดการคลังสินค้า \> ทั่วไป \> รายละเอียดงาน**
1. เลือกกล่องกาเครื่องหมาย **แสดงที่ปิด** ที่ด้านบนของกริด
1. ตั้งค่าตัวกรองคอลัมน์ **ชนิดใบสั่งงาน** เป็น *ความเคลื่อนไหวของสินค้าคงคลัง*

    ระบบตรวจพบการตรวจนับนี้เป็นความเคลื่อนไหวของสินค้าคงคลังโดยอัตโนมัติ ความเคลื่อนไหวนี้อนุญาตเนื่องจากตัวเลือก **อนุญาตให้ย้ายป้ายทะเบียนระหว่างการตรวจนับตามรอบ** ตั้งค่าเป็น *ใช่* สำหรับคลังสินค้า *61* บนหน้า **คลังสินค้า**

## <a name="scenario-4-define-cycle-count-thresholds"></a>สถานการณ์ที่ 4: กําหนดขีดจำกัดการตรวจนับตามรอบ

วิธีการหนึ่งในการสร้างงานการตรวจนับตามรอบคือการใช้ขีดจำกัด ขีดจำกัดการตรวจนับตามรอบบ่งชี้ขีดจำกัดปริมาณหรือเปอร์เซ็นต์ของสินค้าในสินค้าคงคลัง งานการตรวจนับตามรอบถูกสร้างขึ้นโดยอัตโนมัติเมื่อถึงขีดจำกัด

ตัวอย่างเช่น มีสินค้า 60 รายการในสถานที่ที่มีขีดจำกัดการตรวจนับตามรอบคือ 40 ในระหว่างธุรกรรมใบสั่งขาย สินค้า 25 รายการจะถูกเบิกจากสถานที่ และเก็บไว้ในสถานที่การจัดเตรียม เนื่องจากจำนวนสินค้าใหม่ 35 รายการน้อยกว่าปริมาณขีดจำกัด งานการตรวจนับตามรอบจะมีการสร้างโดยอัตโนมัติสำหรับสถานที่

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าขีดจำกัดการตรวจนับตามรอบ

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การตรวจนับตามรอบ \> ขีดจำกัดการตรวจนับตามรอบ**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างขีดจำกัด และตั้งค่าค่าต่อไปนี้:

    - **รหัสขีดจำกัดการตรวจนับตามรอบ:** *L0101*
    - **รายละเอียด:** *ขีดจำกัด L0101*
    - **ปริมาณขีดจำกัด:** *2*
    - **หน่วย:** *ea*
    - **ขีดจำกัดกำลังการผลิตตามเปอร์เซ็นต์:** *0.00*
    - **ชนิดขีดจำกัดการตรวจนับตามรอบ:** *ปริมาณ*
    - **ประมวลผลการตรวจนับตามรอบทันที:** *ใช่*
    - **จำนวนวันระหว่างการตรวจนับตามรอบ:** *1*
    - **รหัสกลุ่มงาน:** *CycleCount*

1. บนบานหน้าต่างการดำเนินการ เลือก **เลือกสินค้า**
1. ในกล่องโต้ตอบตัวแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้ค้นหาแถวที่มีการตั้งค่า **ฟิลด์** เป็น *หมายเลขสินค้า* ตั้งค่าฟิลด์ **เงื่อนไข** สำหรับแถวนั้นเป็น *L0101*
1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม

    ขณะนี้คุณได้กําหนดขีดจำกัดการตรวจนับตามรอบของสินค้า *L0101* แล้ว

ขณะนี้จะมีการสร้างการตรวจนับตามรอบขึ้นเนื่องจากสินค้า *L0101* ที่สถานที่ใดๆ ถ้าปริมาณคงคลังคงเหลือน้อยกว่า 2 และถ้าวันที่ของการตรวจนับตามรอบล่าสุดของสถานที่ไม่ใช่วันนี้

## <a name="scenario-5-define-cycle-count-plans"></a>สถานการณ์ที่ 5: กําหนดแผนการตรวจนับตามรอบ

แผนการตรวจนับตามรอบช่วยให้คุณสามารถสร้างงานการตรวจนับตามรอบโดยอัตโนมัติได้ คุณสามารถตั้งค่าแผนการตรวจนับตามรอบแต่ละแผนด้วยการสอบถามเกี่ยวกับสินค้าและที่ตั้งเฉพาะ เมื่อชุดงานรัน ชุดงานจะสร้างงานการตรวจนับตามรอบให้กับสถานที่ทั้งหมดที่ตรงกับเกณฑ์สินค้าและสถานที่ตั้ง (สูงสุดตามจํานวนการตรวจนับสูงสุดที่ระบุไว้ของแผน) เมื่อมีสร้างงานการตรวจนับตามรอบ งานที่ตรวจนับจะรวมข้อมูลเกี่ยวกับที่ตั้งที่ต้องตรวจนับ สินค้าคงคลังคงเหลือซึ่งสัมพันธ์ด้วยที่สถานที่ไม่ถูกบล็อก ดังนั้นจึงพร้อมใช้งานเฉพาะกับการประมวลผลการจองและขาออก แม้ว่าจะมีงานการตรวจนับที่เปิดอยู่

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าแผนการตรวจนับตามรอบ

1. ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การตรวจนับตามรอบ \> แผนการตรวจนับตามรอบ**
1. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด และจากนั้น ตั้งค่าต่อไปนี้:

    - **รหัสแผนการตรวจนับตามรอบ:** *BULK06*
    - **คำอธิบาย:** *การตรวจนับของสถานที่เก็บ BULK06*
    - **รหัสกลุ่มงาน:** *CycleCount*
    - **จำนวนการตรวจนับตามรอบสูงสุด:** *10*
    - **จำนวนวันระหว่างการตรวจนับตามรอบ:** *10*
    - **สถานที่ว่างเปล่า:** *ไม่รวมว่างเปล่า*
    - **เทมเพลตงาน** ปล่อยฟิลด์นี้ว่างไว้ได้

1. บนบานหน้าต่างการดำเนินการ เลือก **เลือกสถานที่**
1. กล่องโต้ตอบตัวแก้ไขการสอบถามมาตรฐานจะปรากฏขึ้น บนแท็บ **ช่วง** เพิ่มแถว และตั้งค่าต่อไปนี้:

    - **ตาราง:** *สถานที่*
    - **ฟิลด์:** *รหัสโซน*
    - **เกณฑ์:** *BULK06*

1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม
1. ในบานหน้าต่างการดำเนินการ เลือก **ดำเนินการตามแผนการตรวจนับตามรอบ**
1. ในกล่องโต้ตอบ **แผนการตรวจนับตามรอบ** บนแท็บด่วน **รันในพื้นหลัง** ให้ตั้งค่าตัวเลือก **การประมวลผลชุดงาน** เป็น *ใช่*
1. เลือก **การเกิดซ้ำ**
1. ในกล่องโต้ตอบ **กําหนดการเกิดซ้ำ** ให้ตั้งค่าชุดงานเพื่อให้ชุดงานเริ่มต้นทันทีและรันทันทีทุกนาที และเพื่อให้ไม่มีวันที่สิ้นสุด
1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **กําหนดการเกิดซ้ำ**
1. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **แผนการตรวจนับตามรอบ**

    ข้อความจะแจ้งให้คุณทราบว่างานถูกเพิ่มเข้าในคิวชุดงานแล้ว

1. ไปที่ **การจัดการคลังสินค้า \> ทั่วไป \> จัดกำหนดการตรวจนับตามรอบ** แผนจะเริ่มต้นในทันทีและสร้างงานการตรวจนับ เนื่องจากงานการตรวจนับยังไม่เสร็จสมบูรณ์ ฟิลด์ **สถานะ** ถูกตั้งค่าเป็น *ระหว่างกระบวนการ* หลังจากหนึ่งนาที ค่าในคอลัมน์ **การตรวจนับตามรอบรวม** จะเปลี่ยนเป็น *1*

    > [!NOTE]
    > งานการตรวจนับตามรอบจะไม่ถูกสร้างขึ้น ถ้าจํานวนวันนับตามรอบล่าสุดน้อยกว่าค่าที่คุณตั้งค่าไว้เป็นฟิลด์ **วันระหว่างการตรวจนับตามรอบ** ของแผนการตรวจนับตามรอบ ตัวอย่างเช่น ถ้าฟิลด์ **จำนวนวันระหว่างการตรวจนับตามรอบ** ถูกตั้งค่าเป็น *5* งานการตรวจนับตามรอบจะถูกสร้างทุกๆ ห้าวัน อย่างไรก็ตาม ถ้างานการตรวจนับตามรอบมีการประมวลผลในวันที่ 3 วงานการตรวจนับตามรอบจะมีการสร้างในห้าวันหลังจากการตรวจนับตามรอบล่าสุดถูกประมวลผลในวันที่ 8

1. ในบานหน้าต่างการดำเนินการ เลือก **งาน** เพื่อดูงานการตรวจนับที่สร้างขึ้นแล้ว
