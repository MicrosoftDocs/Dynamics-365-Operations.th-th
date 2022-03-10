---
title: รวม Dynamics 365 Supply Chain Management (การจัดการสินทรัพย์) ด้วย Dynamics 365 Guides
description: หัวข้อนี้อธิบายถึงวิธีการรวมโมดูลการจัดการสินทรัพย์ใน Microsoft  Dynamics 365 Supply Chain Management ด้วย Dynamics 365 Guides เพื่อใช้ประโยชน์จากคู่มือแบบผสมความจริงในการให้บริการและลำดับงานการบำรุงรักษาในแต่ละวัน
author: johanhoffmann
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 4132992eb5f4b42d43d9ff72cada616fe0573c2f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568266"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>รวม Dynamics 365 Supply Chain Management (การจัดการสินทรัพย์) ด้วย Dynamics 365 Guides

[!include [banner](../includes/banner.md)]

คุณสามารถรวมโมดูล **การจัดการสินทรัพย์** ใน Microsoft Dynamics 365 Supply Chain Management ด้วย Dynamics 365 Guides เพื่อใช้ประโยชน์จากคู่มือแบบผสมความจริงในการให้บริการและลำดับงานการบำรุงรักษาในแต่ละวัน ถ้าคู่มือเชื่อมโยงกับใบสั่งงานการจัดการสินทรัพย์ ผู้ปฏิบัติงานที่เปิดรายการตรวจสอบการบำรุงรักษาของใบสั่งงานในแอป Supply Chain Management (Dynamics 365) สำหรับอุปกรณ์เคลื่อนที่เห็นว่าคู่มือจะพร้อมใช้งาน ผู้ปฏิบัติงานสามารถค้นหา และเปิดคู่มือในแอป Dynamics 365 Guides HoloLens

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะสามารถแนบคู่มือกับใบสั่งงานการจัดการสินทรัพย์ คุณต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้ให้สมบูรณ์:

- [ตั้งค่า Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) รุ่น 10.0.9 หรือใหม่กว่า
- [เปิดใช้งานการรวมแบบสองทิศทางสำหรับแอป Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)
- [เปิดใช้งานการบิน](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) สำหรับคุณลักษณะ  **MRGuidesFeature** (สำหรับสภาพแวดล้อมการผลิต คุณต้องส่งตั๋วสนับสนุน เพื่อให้ผู้เช่าของคุณถูกเพิ่มลงในกลุ่มการบิน)
- [เปิดใช้งานคีย์การตั้งค่าคอนฟิกต่อไปนี้](/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) บนหน้า **การตั้งค่าคอนฟิกลิขสิทธิ์** :

    - การบริหารสินทรัพย์ \> การบริหารสินทรัพย์ความเป็นจริงผสม
    - ความเป็นจริงผสม \> คู่มือความเป็นจริงผสม

- [ตั้งค่า Dynamics 365 Guides](/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) รุ่น 200.0.0.96 หรือใหม่กว่า

## <a name="use-dynamics-365-guides-with-asset-management"></a>ใช้ Dynamics 365 Guides กับการจัดการสินทรัพย์

เมื่อต้องการเชื่อมโยงคู่มือ ให้คุณใช้บรรทัดรายการตรวจสอบการบำรุงรักษาในการบริหารสินทรัพย์ คุณสามารถสร้างความสัมพันธ์ผ่านแม่แบบใบสั่งรายการตรวจสอบการบำรุงรักษา ชนิดงานการบำรุงรักษา หรือใบสั่งงาน เนื่องจากมีบรรทัดรายการตรวจสอบการบำรุงรักษาทั้งสามรายการ คุณสามารถประหยัดเวลาโดยใช้แม่แบบได้ เนื่องจากแม่แบบจะเชื่อมโยงกับชนิดงานการบำรุงรักษาทั้งหมดที่ใช้ ตัวอย่างเช่น คู่มือที่เชื่อมโยงกับชนิดงานการบำรุงรักษาจะเชื่อมโยงกับใบสั่งงานทั้งหมดที่ระบุชนิดงานนั้นโดยอัตโนมัติ ในทางกลับกัน คู่มือที่เชื่อมโยงกับโดยตรงกับใบสั่งงานมีอยู่เฉพาะในใบสั่งงานนั้นเท่านั้น

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>เชื่อมโยงคู่มือกับแม่แบบรายการตรวจสอบการบำรุงรักษา

เมื่อต้องการเชื่อมโยงคู่มือกับแม่แบบรายการตรวจสอบการบำรุงรักษา ให้ทำตามขั้นตอนต่อไปนี้

1. สร้างคู่มือโดยใช้แอป Dynamics 365 Guides PC และแอป HoloLens สำหรับข้อมูลเกี่ยวกับวิธีสร้างคูมือ ให้ดูหัวข้อต่อไปนี้:

    - [ใช้แอป PC เพื่อสร้างคู่มือ](/dynamics365/mixed-reality/guides/pc-app-overview)
    - [ใช้แอป HoloLens เพื่อวางโฮโลแกรมของคุณ](/dynamics365/mixed-reality/guides/hololens-app-overview)

1. ใน Supply Chain Management ให้ [สร้างแม่แบบรายการตรวจสอบการบำรุงรักษา](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template)
1. เชื่อมโยงคู่มือที่คุณสร้างด้วยบรรทัดรายการตรวจสอบการบำรุงรักษาในแม่แบบรายการตรวจสอบการบำรุงรักษาใหม่:

    1. บนแท็บด่วน **บรรทัดรายการตรวจสอบการบำรุงรักษา** ให้เลือกรายการที่คุณต้องการเชื่อมโยงกับคู่มือ
    1. บนแท็บด่วน **คู่มือที่เชื่อมโยง** ให้เลือก **เพิ่มคู่มือ**

        ![เชื่อมโยงคู่มือกับบรรทัดรายการตรวจสอบการบำรุงรักษา](media/am-guides-integration-add-guide.png "เชื่อมโยงคู่มือกับบรรทัดรายการตรวจสอบการบำรุงรักษา")

    1. ในฟิลด์ **ชื่อ** ให้เลือกคู่มือ แล้วเลือก **บันทึก**

        ![เลือกคู่มือในฟิลด์ชื่อ](media/am-guides-integration-select-guide.png "เลือกคู่มือในฟิลด์ชื่อ")

1. เชื่อมโยงแม่แบบรายการตรวจสอบการบำรุงรักษากับชนิดงาน:

    1. [สร้างชนิดงานการบำรุงรักษา](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) หรือเลือกชนิดงานบำรุงรักษาที่มีอยู่
    1. บนบานหน้าต่างการดำเนินการ ให้เลือก **ค่าเริ่มต้นของชนิดงานการบำรุงรักษา**

        ![ปุ่มค่าเริ่มต้นของชนิดงานการบำรุงรักษา](media/am-guides-integration-job-defaults.png "ปุ่มค่าเริ่มต้นของชนิดงานการบำรุงรักษา")

    1. สร้างบรรทัด แล้วเลือก **บันทึก**

        ![สร้าง บรรทัด](media/am-guides-integration-add-line.png "สร้างบรรทัด")

    1. ในบานหน้าต่างการดำเนินการ เลือก **รายการตรวจสอบการบำรุงรักษา**

        ![ปุ่มรายการตรวจสอบการบำรุงรักษา](media/am-guides-integration-maintenance-checklist.png "ปุ่มรายการตรวจสอบการบำรุงรักษา")

    1. บนแท็บด่วน **บรรทัดรายการตรวจสอบการบำรุงรักษา** เพิ่มบรรทัด แล้วเปลี่ยนค่าของฟิลด์ **ชนิด** เป็น **แม่แบบ**

        ![เปลี่ยนค่าชนิด](media/am-guides-integration-checklist-lines.png "เปลี่ยนค่าชนิด")

    1. บนแท็บด่วน **รายละเอียดของรายการ** ในฟิลด์ **แม่แบบ** ให้เลือกแม่แบบที่คุณเชื่อมโยงคู่มือด้วย แล้วเลือก **บันทึก**

        ![เลือกแม่แบบ](media/am-guides-integration-checklist-line-details.png "เลือกแม่แบบ")

1. [สร้างใบสั่งงาน](work-orders/manually-created-workorders.md#create-work-order) แล้วเลือกชนิดงานการบำรุงรักษาที่ใช้แม่แบบรายการตรวจสอบการบำรุงรักษาที่คุณเชื่อมโยงกับคู่มือ คู่มือถูกเชื่อมโยงกับใบสั่งงานโดยอัตโนมัติ

    ![เลือกชนิดของงานบำรุงรักษา](media/am-guides-integration-create-work-order.png "เลือกชนิดของงานบำรุงรักษา")

1. ดูคู่มือที่เชื่อมโยงกับใบสั่งงานและผู้ปฏิบัติงาน

    1. เปิด [พื้นที่ทำงานแบบเคลื่อนที่ในการจัดการสินทรัพย์](asset-management-mobile-workspace.md) เพื่อเข้าถึงใบสั่งงาน
    1. [เปิดรายการตรวจสอบการบำรุงรักษา](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) สำหรับใบสั่งงาน
    1. เลือกรายการตรวจสอบเพื่อดูคู่มือที่เกี่ยวข้อง

        ![คู่มือที่เชื่อมโยงกับรายการตรวจสอบ](media/am-guides-integration-show-guide.png "คู่มือที่เชื่อมโยงกับรายการตรวจสอบ")

    1. เปิดคู่มือบน HoloLens

        ![เปิดคู่มือบน HoloLens](media/am-guides-integration-hololens-select.png "เปิดคู่มือบน HoloLens")

> [!NOTE]
> นอกจากนี้คุณยังสามารถเชื่อมโยงคู่มือในรายการตรวจสอบการบำรุงรักษาของใบสั่งงานหรือชนิดงานได้โดยตรง

> [!IMPORTANT]
> มีปัญหาที่ทราบ ซึ่งเมื่อคุณเชื่อมโยแม่แบบรายการตรวจสอบการบำรุงรักษากับชนิดงานการบำรุงรักษาเริ่มต้น คู่มือที่เชื่อมโยงกับเแม่แบบจะไม่แสดงอยู่บนแท็บด่วน **คู่มือที่เชื่อมโยง** ของหน้า **ค่าเริ่มต้นของชนิดงานการบำรุงรักษา** อย่างไรก็ตาม คู่มือจะปรากฏขึ้นหลังจากชนิดงานนั้นถูกนำไปใช้กับใบสั่งงานบนแท็บด่วน **คู่มือที่เชื่อมโยง**

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ภาพรวมของการรวมแบบสองทิศทาง](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [ภาพรวมของการจัดการสินทรัพย์](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]