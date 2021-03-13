---
title: Cloud และ edge scale unit สำหรับปริมาณงานในการจัดการการผลิตและคลังสินค้า
description: หัวข้อนี้จะนำเสนอข้อมูลเกี่ยวกับ Cloud และ edge scale unit สำหรับปริมาณงานในการจัดการการผลิตและคลังสินค้า
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 28301cdfb86d00ea6f04e996fe7fb1485e83b2d4
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104975"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Cloud และ edge scale unit สำหรับปริมาณงานในการจัดการการผลิตและคลังสินค้า

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Cloud และ edge scale unit เปิดใช้งานการกระจายปริมาณงานการดำเนินการของการผลิตและคลังสินค้าในระหว่างสภาพแวดล้อมที่แตกต่างกัน ฟังก์ชันนี้จะช่วยปรับปรุงประสิทธิภาพการทำงาน ป้องกันการขัดจังหวะการบริการ และเพิ่มความพร้อมในการทำงาน มีให้โดย Add-in ต่อไปนี้:

- Add-in ของ Cloud Scale Unit สำหรับ Dynamics 365 Supply Chain Management
- Add-in ของ Edge Scale Unit สำหรับ Dynamics 365 Supply Chain Management

บริษัทที่ทำงานกับการผลิตและการกระจายสินค้าต้องสามารถรันกระบวนการทางธุรกิจที่สำคัญได้ 24/7 โดยไม่มีการขัดจังหวะและที่ Scale Cloud และ edge scale unit เปิดใช้งานให้บริษัทรันภารกิจหลักของการประมวลผลการผลิตและคลังสินค้าโดยไม่มีการขัดจังหวะ แม้กระทั่งเมื่อประสบกับปัญหาการเชื่อมต่อเครือข่ายหรือเวลาแฝงเป็นครั้งคราว

## <a name="public-preview-information"></a>ข้อมูลตัวอย่างสำหรับสาธารณะ

การแสดงตัวอย่างจะให้สภาพแวดล้อมหนึ่งที่ทำหน้าที่เป็นฮับที่ใช้ cloud ของสภาพแวดล้อม Dynamics 365 Supply Chain Management ของคุณ และสภาพแวดล้อมหนึ่งที่ทำหน้าที่เป็น Cloud Scale Unit

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>ดูตัวอย่างความพร้อมใช้งาน

ตัวอย่างสำหรับ Cloud และ edge scale unit จะพร้อมใช้งานสำหรับลูกค้าที่มีอยู่ของ Supply Chain Management ในเดือนตุลาคม 2020

การเข้าถึงตัวอย่างเดือนตุลาคม รุ่น 10.0.15/ การอัพเดปแพลตฟอร์ม 39 สำหรับการปรับใช้ ในสภาพแวดล้อม [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) ของคุณ คุณต้องเป็นส่วนหนึ่งของโปรแกรมการนำการแสดงตัวอย่างก่อนมาใช้ (หรือที่เรียกอีกอย่างว่า PEAP) สำหรับ Supply Chain Management คุณสามารถเข้าร่วม PEAP ได้ถ้าคุณเป็นสมาชิกของ [Dynamics Insider Program](https://experience.dynamics.com/insider) ที่กว้างขึ้น เพียงแค่เลือกโปรแกรมเฉพาะที่มีชื่อว่า "Finance & Operations: โปรแกรมการนำการแสดงตัวอย่างก่อนมาใช้ (PEAP)"

> [!IMPORTANT]
> ความสามารถของ scale unit สำหรับ Supply Chain Management มีอยู่เฉพาะเมื่อคุณยอมรับ [เงื่อนไขการแสดงตัวอย่างของ Cloud + Edge สำหรับ Finance and Operations](https://Aka.ms/SCMCnETerms) เท่านั้น

### <a name="data-processing-for-the-preview"></a>การประมวลผลข้อมูลสำหรับการแสดงตัวอย่าง

ในระหว่างการแสดงตัวอย่างสำหรับสาธารณะ บางบริการจะมีโฮสต์อยู่ในสหรัฐอเมริกาเท่านั้น อย่างไรก็ตาม เมื่อคุณลักษณะที่พร้อมใช้งานโดยทั่วไป การให้บริการการจัดการเหล่านี้จะพร้อมใช้งานในเขตภูมิศาสตร์ทั้งหมดที่ได้รับการสนับสนุนโดย Supply Chain Management การทำเช่นนี้จะมีผลกระทบต่อการโอนย้ายและการจัดเก็บข้อมูลการจัดการที่ใช้โดยผู้จัดการ scale unit รวมถึง:

- ชื่อผู้เช่าและรหัสของคุณ
- รหัสโครงการ LCS ของคุณ
- อีเมลของผู้ดูแลระบบที่ใช้ในการล็อกอิน
- รหัสสภาพแวดล้อมสำหรับฮับและ scale unit
- การตั้งค่าคอนฟิกปริมาณงาน
- การรวบรวมเกณฑ์ชี้วัด (เช่น เวลาแฝง และปริมาณที่สามารถประมวลผลได้) ซึ่งแสดงอยู่บนหน้าการวิเคราะห์แผนที่

ข้อมูลที่โอนย้ายไปและจัดเก็บไว้ในศูนย์ข้อมูลของสหรัฐอเมริกาจะถูกลบออกเมื่อสภาพแวดล้อมการแสดงตัวอย่างของคุณปิดลง

### <a name="sign-up-for-the-preview"></a>ลงทะเบียนรุ่นตัวอย่าง

การลงชื่อสมัครใช้การแสดงตัวอย่าง Cloud และ edge สำหรับ Supply Chain Management องค์กรของคุณต้องมีสภาพแวดล้อมระบบคลาวด์สำหรับ Supply Chain Management อยู่แล้ว

ความสามารถ scale unit มีอยู่ในตัวอย่างสำหรับสาธารณะในขณะนี้ เมื่อคุณลงชื่อสมัครใช้ คุณต้องใช้บัญชีผู้ใช้ในผู้เช่าเฉพาะ นอกจากนี้คุณต้องเป็นเจ้าของโครงการหรือผู้ดูแลระบบสภาพแวดล้อมใน LCS สำหรับโครงการ Dynamics 365 LCS ที่ใช้งานอยู่ในผู้เช่ารายนั้น

เมื่อคุณลงชื่อสมัครใช้การแสดงตัวอย่าง คุณจะต้องเลือกผู้เช่าและไปที่ขั้นตอนการลงทะเบียน ทันทีที่ Microsoft สามารถปันส่วนกำลังการผลิตของการแสดงตัวอย่าง เราจะส่งอีเมลที่รวมรายละเอียดการเตรียมใช้งานและรหัสโปรโมชัน (promo) สำหรับสองสภาพแวดล้อม (ฮับ และ scale unit) สำหรับโครงการ LCS ที่เหมาะสม จากนั้นคุณจะสามารถปรับใช้สภาพแวดล้อมสองอย่างเป็นสภาพแวดล้อม sandbox ระดับ2 สภาพแวดล้อมดังกล่าวจะมีผลบังคับใช้ 60 วัน นับจากวันที่สร้างรหัสโปรโมชัน คุณไม่ควรใช้สภาพแวดล้อมทั้งสอง จนกว่าขั้นตอนที่อธิบายไว้ในย่อหน้าถัดไปได้เสร็จสมบูรณ์แล้ว

หลังจากที่คุณยืนยันกับ Microsoft ว่าได้มีการปรับใช้สองสภาพแวดล้อมโดยใช้รหัสโปรโมชัน สภาพแวดล้อมหนึ่งจะมีการตั้งค่าคอนฟิกให้ทำงานเป็นฮับ และอีกสภาพแวดล้อมจะมีการตั้งค่าคอนฟิกให้ทำงานเป็น scale unit จากนั้นคุณสามารถตั้งค่าคอนฟิก scale unit และปรับใช้ปริมาณงานการจัดการคลังสินค้าและการผลิตที่เลือก โดยใช้ [พอร์ทัล Scale Unit Manager](https://aka.ms/SCMSUM)

สภาพแวดล้อมการแสดงตัวอย่างจะถูกลบออกโดยอัตโนมัติหลังจาก 60 วัน อย่างไรก็ตาม สภาพแวดล้อมเหล่านั้นอาจถูกลบอย่างเร็วถ้าปรากฏว่าไม่มีการใช้งานอยู่ หลังจากลบสภาพแวดล้อมการแสดงตัวอย่างของคุณแล้ว คุณสามารถลงชื่อสมัครใช้และคิวสำหรับการปรับใช้การแสดงตัวอย่างใหม่

การลงชื่อสมัครใช้การแสดงตัวอย่าง ให้ไปที่ [พอร์ทัล Scale Unit Manager](https://aka.ms/SCMSUM)

### <a name="limitations-that-apply-during-the-preview-period"></a>ข้อจำกัดที่ใช้ในระหว่างรอบระยะเวลาการแสดงตัวอย่าง

> [!IMPORTANT]
> สำหรับระยะเริ่มต้นของโปรแกรมการแสดงตัวอย่างสำหรับคุณลักษณะนี้ Microsoft จะสนับสนุนเแพาะฮับที่มี cloud scale unit เท่านั้น ไม่ใช่ฮับที่มี edge scale unit Edge scale unit มีการติดตั้งแบบในสถานที่ และคาดว่าจะพร้อมใช้งานระหว่างระยะที่กำลังจะมาถึงของโปรแกรม

เนื่องจาก cloud และ edge scale unit คือคุณลักษณะการแสดงตัวอย่าง การบริการที่เกี่ยวข้องกับรายการนั้นจะมีอยู่ในประเทศและภูมิภาคที่จำกัด โดยการเปิดใช้งาน cloud และ edge scale unit คุณยืนยันว่าคุณเข้าใจว่าข้อมูลบางอย่างที่เกี่ยวข้องกับการตั้งค่าคอนฟิกและการประมวลผลของ cloud และ edge scale unit อาจจัดเก็บอยู่ในศูนย์ข้อมูลที่อยู่ในสหรัฐอเมริกา เมื่อเปิดใช้งาน cloud และ edge scale unit คุณเห็นด้วยกับการ [เงื่อนไข Cloud + Edge Preview สำหรับ Finance and Operations](https://Aka.ms/SCMCnETerms) หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับ cloud and edge scale unit โปรดดูที่ [คู่มือ](https://aka.ms/scmcne)

ความเป็นส่วนตัวของคุณมีความสำคัญต่อ Microsoft เรียนรู้เพิ่มเติม อ่าน [คำชี้แจงสิทธิส่วนบุคคล](https://aka.ms/privacy) ของเรา

> [!IMPORTANT]
> ฟังก์ชันธุรกิจบางอย่างไม่ได้รับการสนับสนุนอย่างเต็มที่ในตัวอย่างสำหรับสาธารณะเมื่อมีการใช้ปริมาณงานบน scale unit สำหรับข้อมูลเพิ่มเติมเกี่ยวกับปริมาณงานการใช้งาน ให้ดูที่ส่วนต่อไปนี้ในหัวข้อนี้

## <a name="scale-units-and-dedicated-workloads"></a>Scale unit และปริมาณงานที่จัดสรรไว้

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 กับ scale unit":::

Scale unit ขยายสภาพแวดล้อมฮับ Supply Chain Management ส่วนกลางของคุณ โดยการเพิ่มความสามารถการประมวลผลที่เฉพาะเจาะจง Scale unit สามารถรันได้ใน cloud อีกทางหนึ่งคือ คุณสามารถรันบน edge ที่สถานที่อำนวยความสะดวกท้องถิ่นของคุณได้ Scale unit สามารถยกเลิกการเชื่อมต่อจากสภาพแวดล้อมฮับชั่วคราวได้ เมื่อมีการเชื่อมต่อ Scale unit จะรับข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการรันการประมวลผลเฉพาะสำหรับปริมาณงานที่กำหนด

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="ตัวเลือก Scale unit ในตัวอย่างสำหรับสาธารณะ":::

สำหรับตัวอย่างสำหรับสาธารณะ คุณสามารถตั้งค่าคอนฟิกสภาพแวดล้อมฮับกับปริมาณงานที่เลือกบน cloud scale unit โดยใช้พอร์ทัล Scale Unit Manager แสดงตัวอย่างผู้เข้าร่วมที่มีสิทธิ์เข้าถึงสภาพแวดล้อมในสถานที่ของข้อมูลทางธุรกิจ (LBD) นอกจากนี้ยังสามารถตั้งค่าคอนฟิกสภาพแวดล้อม LBD เป็น edge scale unit

ปริมาณงานเป็นชุดที่กำหนดของฟังก์ชันธุรกิจซึ่งสามารถแยกออกและมอบหมายให้กับ scale unit ในปัจจุบัน คุณลักษณะการแสดงตัวอย่างมีสองชนิดของปริมาณงาน:

- การดำเนินการผลิต
- การจัดการคลังสินค้า

คุณสามารถกำหนดหนึ่งคุณลักษณะของปริมาณงานแต่ละชนิดต่อ scale unit 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>ความสามารถในการดำเนินงานของปริมาณงานการผลิตเฉพาะใน scale unit

สำหรับการดำเนินการผลิต cloud และ edge scale unit จัดส่งความสามารถต่อไปนี้ ถึงแม้ว่า edge unit จะไม่ได้เชื่อมต่อกับ cloud:

- ผู้ปฏิบัติงานเครื่องจักรและหัวหน้างานฝ่ายผลิตสามารถเข้าถึงแผนการผลิตที่มีการดำเนินงาน
- ผู้ปฏิบัติงานในเครื่องสามารถรักษาแผนให้ทันสมัยอยู่เสมอโดยการรันงานการผลิตที่แยกต่างหากและมีการประมวลผล
- หัวหน้างานฝ่ายผลิตสามารถปรับปรุงแผนการดำเนินงานได้
- ผู้ปฏิบัติงานสามารถเข้าถึงเวลาและการเข้างานสำหรับการตอกบัตรเข้าและการตอกบัตรออกบน edge เพื่อให้มั่นใจว่าการคำนวณการจ่ายค่าจ้างของผู้ปฏิบัติงานถูกต้อง

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รายละเอียดปริมาณงาน scale unit ของการผลิต](cloud-edge-workload-manufacturing.md)

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>ความสามารถในการจัดการของปริมาณงานการผลิตเฉพาะใน scale unit

สำหรับการจัดการคลังสินค้า cloud และ edge scale unit จัดส่งความสามารถต่อไปนี้ ถึงแม้ว่า edge unit จะไม่ได้เชื่อมต่อกับ cloud:

- การประมวลผลวิธีการเวฟที่เลือกเปิดใช้งานสำหรับใบสั่งขายและการเติมสินค้าตามความต้องการ
- ผู้ปฏิบัติงานคลังสินค้าสามารถรันงานคลังสินค้าสำหรับการขายและการเติมสินค้าตามความต้องการ โดยใช้แอปคลังสินค้า
- ผู้ปฏิบัติงานคลังสินค้าสามารถสอบถามปริมาณคงคลังคงเหลือได้โดยใช้แอปคลังสินค้า
- ผู้ปฏิบัติงานคลังสินค้าสามารถสร้างและรันการโยกย้ายปริมาณคงคลังคงเหลือได้ โดยใช้แอปคลังสินค้า
- ผู้ปฏิบัติงานคลังสินค้าสามารถลงทะเบียนใบสั่งซื้อและทำการสำรองสินค้า โดยใช้แอปคลังสินค้า

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รายละเอียดปริมาณงาน scale unit ของคลังสินค้า](cloud-edge-workload-warehousing.md)

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Onboard scale unit สำหรับสภาพแวดล้อม Supply Chain Management ของคุณ

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>ปรับใช้การแสดงตัวอย่างสำหรับ cloud และ edge scale unit

ภาพประกอบต่อไปนี้แสดงโฟลว์การลงทะเบียนและการเตรียมใช้งานสำหรับตัวอย่างสำหรับสาธารณะ สำหรับ cloud scale unit

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="ขั้นตอนการลงทะเบียนการแสดงตัวอย่าง":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>เลือกผู้เช่าโครงการ LCS ของคุณ และกระบวนการแสดงตัวอย่างโดยละเอียด

ในการแสดงตัวอย่างสาธารณะ [พอร์ทัล Scale Unit Manager](https://aka.ms/SCMSUM) แสดงรายชื่อผู้เช่าซึ่งบัญชีของคุณเป็นส่วนหนึ่ง และคุณเป็นเจ้าของหรือผู้ดูแลระบบสภาพแวดล้อมสำหรับโครงการ LCS

ถ้าผู้เช่าที่คุณกำลังค้นหาไม่ได้อยู่ในรายการนี้ ให้ไปที่ [LCS](https://lcs.dynamics.com/v2) และตรวจสอบให้แน่ใจว่าคุณเป็นผู้ดูแลระบบสภาพแวดล้อมหรือเจ้าของโครงการของโครงการ LCS สำหรับผู้เช่ารายนั้น โปรดทราบว่า เฉพาะบัญชี Azure Active Directory (Azure AD) จากผู้เช่าที่เลือกเท่านั้นที่จะได้รับอนุญาตให้ทำการลงทะเบียนได้

> [!NOTE]
> หลังจากที่คุณใช้การเปลี่ยนแปลงกับ LCS อาจใช้เวลานานถึง 30 นาที สำหรับรายชื่อผู้เช่าเพื่อให้สะท้อนถึงการเปลี่ยนแปลง

สำหรับผู้เช่าแต่ละราย รายการจะแสดงสถานะของการลงทะเบียน

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="ตัวเลือกลงทะเบียนสำหรับผู้เช่า":::

เลือกลิงค์ **คลิกที่นี่เพื่อลงทะเบียน** เพื่อลงทะเบียนผู้เช่า LCS ของคุณ เพื่อเข้าร่วมในการแสดงตัวอย่าง คุณต้องยอมรับเงื่อนไข นอกจากนี้คุณต้องจัดหาที่อยู่อีเมลสำหรับธุรกิจโดย Microsoft สามารถส่งการติดต่อสื่อสารที่เกี่ยวข้องกับกระบวนการลงทะเบียนการแสดงตัวอย่าง

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="การส่งลงทะเบียนสำหรับผู้เช่า":::

Microsoft จะตรวจสอบความถูกต้องของคำขอของคุณและแจ้งให้คุณทราบขั้นตอนถัดไป โดยการส่งอีเมลไปยังที่อยู่ที่คุณป้อนไว้ในแบบฟอร์มการลงทะเบียน

หลังจากที่คุณได้รับอนุญาตให้เข้าถึงโปรแกรมแสดงตัวอย่างแล้ว คุณจะได้รับรหัสโปรโมชันสองรหัสสำหรับโครงการ LCS ของคุณ ขณะนี้คุณสามารถใช้รหัสโปรโมชันเหล่านั้นเพื่อปรับใช้สภาพแวดล้อมสองอย่างใน LCS สภาพแวดล้อมต้องใช้ใช้ PEAP รุ่น 10.0.15 หรือใหม่กว่า เมื่อคุณใช้รหัสโปรโมชันเสร็จเรียบร้อยแล้ว ให้แจ้ง Microsoft (ตามที่แนะนำ) เพื่อให้เราสามารถเปิดใช้งานสภาพแวดล้อมสำหรับคุณลักษณะการแสดงตัวอย่างให้เสร็จสมบูรณ์ Microsoft จะแจ้งให้คุณทราบเมื่อขั้นตอนการตั้งค่าคอนฟิกนี้เสร็จสมบูรณ์แล้ว

ขณะนี้คุณสามารถเริ่มต้นการตั้งค่าคอนฟิก scale unit และปริมาณงานในสภาพแวดล้อมการแสดงตัวอย่างของคุณ

> [!IMPORTANT]
> เมื่อคุณตั้งค่าคอนฟิก cloud scale unit คุณสามารถ [ทำตามขั้นตอนทั้งหมดที่จำเป็นในพอร์ทัล Scale Unit Manager](#scale-unit-manager-portal)
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>จัดการ scale unit และปริมาณงานในระบบ cloud โดยใช้พอร์ทัล Scale Unit Manager

ไปที่ [พอร์ทัล Scale Unit Manager](https://aka.ms/SCMSUM) แล้วล็อกอินโดยใช้บัญชีผู้เช่าของคุณ บนหน้า **ตั้งค่าคอนฟิก scale unit** คุณสามารถเพิ่มสภาพแวดล้อมฮับถ้ายังไม่ได้แสดงรายการไว้ คุณสามารถเลือกฮับที่คุณต้องการตั้งค่าคอนฟิกกับ scale unit และปริมาณงาน

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="ประสบการณ์การจัดการ Scale unit และปริมาณงาน":::

เมื่อต้องการเพิ่ม scale unit หนึ่งหน่วยขึ้นไปที่มีอยู่ในโทโพโลยีของคุณ ให้เลือก **เพิ่ม scale unit** ในการแสดงตัวอย่าง คุณควรเห็น cloud scale unit ที่คุณปรับใช้จากรหัสโปรโมชันอย่างใดอย่างหนึ่งที่คุณได้รับเป็นส่วนหนึ่งของโปรแกรมแสดงตัวอย่าง

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

บนแท็บ **ปริมาณงานที่กำหนด** ให้ใช้ปุ่ม **สร้างปริมาณงาน** เพื่อเพิ่มการจัดการคลังสินค้าหรือปริมาณงานการดำเนินการผลิตเป็น scale unit หนึ่งของคุณ สำหรับแต่ละปริมาณงาน คุณต้องระบุบริบทของกระบวนการที่จะเป็นของปริมาณงาน สำหรับปริมาณงานการจัดการคลังสินค้า บริบทคือคลังสินค้าเฉพาะ ในไซต์ที่ระบุ และนิติบุคคล สำหรับปริมาณการดำเนินการผลิต บริบทคือไซต์ที่ระบุ ในนิติบุคคล

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="การสร้างปริมาณงาน":::

> [!IMPORTANT]
> พอร์ทัล Scale Unit Manager ในการแสดงตัวอย่าง ไม่อนุญาตให้คุณลบปริมาณงานออกจาก scale unit หรือยกเลิก scale unit จากฮับ หลังจากที่ทำการกำหนดแล้ว ถ้าคุณต้องลบการกำหนด โปรดติดต่อผู้ติดต่อของคุณ สำหรับการจัดการโปรแกรมการแสดงตัวอย่าง

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->
