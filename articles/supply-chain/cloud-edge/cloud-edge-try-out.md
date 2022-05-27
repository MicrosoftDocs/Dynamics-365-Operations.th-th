---
title: ลองใช้สเกลยูนิตในโทโพโลยีแบบไฮบริดแบบกระจาย
description: หัวข้อนี้จะนำเสนอข้อมูลเกี่ยวกับวิธีการลองใช้สเกลยูนิตในระบบคลาวด์และแบบปลายทางสำหรับปริมาณงานในการจัดการการผลิตและคลังสินค้า
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 658948d94cd012b95812a786433967f5cadc3a15
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711899"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>ลองใช้สเกลยูนิตในโทโพโลยีแบบไฮบริดแบบกระจาย

[!include [banner](../includes/banner.md)]

กระบวนการในการลองใช้การกระจายโทโพโลยีแบบไฮบริดแบบกระจายเป็นเรื่องง่าย ในระหว่างขั้นแรก คุณควรตรวจสอบความถูกต้องของการกำหนดเองเพื่อให้แน่ใจว่ามีการทำงานในโทโพโลยีแบบกระจาย คุณมีตัวเลือกสองแบบ

## <a name="option-1-evaluate-customizations-in-development-environments"></a>ตัวเลือก 1: ประเมินการกำหนดเองในสภาพแวดล้อมการพัฒนา

ก่อนที่คุณจะเริ่มใช้งานสภาพแวดล้อม Sandbox เราขอแนะนำให้คุณสำรวจสเกลยูนิตในการตั้งค่าการพัฒนา เช่น สภาพแวดล้อมแบบ One-Box (หรือที่เรียกว่าสภาพแวดล้อมระดับ 1) เพื่อให้คุณสามารถตรวจสอบความถูกต้องของกระบวนการ การกกำหนดเอง และโซลูชันได้ ในระหว่างขั้นนี้ ข้อมูลและการเลือกกำหนดจะถูกใช้กับสภาพแวดล้อมแบบ One-Box คุณสามารถเรียกใช้ในสภาพแวดล้อมเดียวซึ่งสามารถเป็นทั้งบทบาทฮับองค์กรและสเกลยูนิตได้ หรือคุณสามารถมีสภาพแวดล้อมการพัฒนาสองสภาพแวดล้อม ซึ่งสภาพแวดล้อมหนึ่งรับบทบาทของฮับและอีกสภาพแวดล้อมรับบทบาทของสเกลยูนิต การตั้งค่านี้ช่วยให้สามารถระบุและแก้ปัญหาได้ดีที่สุด นอกจากนี้ [การสร้างพรีวิว](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) ล่าสุดยังสามารถใช้ในการทำตามลำดับขั้นนี้ด้วย

คุณควรใช้ [เครื่องมือการปรับใช้สเกลยูนิตกับสภาพแวดล้อมการพัฒนาแบบ One-Box](https://github.com/microsoft/SCMScaleUnitDevTools) เพื่อติดตั้งและดูแลรักษาสภาพแวดล้อม เครื่องมือเหล่านี้ช่วยให้คุณตั้งค่าคอนฟิกฮับและสเกลยูนิตในหนึ่งหรือสองสภาพแวดล้อมแบบ One-Box เครื่องมือนี้มีให้เป็นทั้งรุ่นฐานสองและในโค้ดต้นฉบับบน GitHub ศึกษา Wiki โครงการ ซึ่งรวมถึง [คู่มือการใช้ขั้นตอนทีละขั้นตอน](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) ที่อธิบายวิธีการใช้เครื่องมือ หากคุณกำลัง [ปรับใช้สเกลยูนิตแบบปลายทางบนฮาร์ดแวร์ที่กำหนดเองโดยใช้ข้อมูลธุรกิจแบบภายในเครื่อง (LBD)](cloud-edge-edge-scale-units-lbd.md) คุณต้องปฏิบัติตามกระบวนการอื่น

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>ตัวเลือก 2: ได้รับ Add-in และปรับใช้ในสภาพแวดล้อม sandbox ของคุณ

เมื่อต้องการลองใช้โทโพโลยีแบบไฮบริดแบบกระจาย คุณต้องมีสภาพแวดล้อม sandbox สองสภาพแวดล้อม (ระดับ 2) โดยสภาพแวดล้อมหนึ่งมีข้อมูลของคุณ (ฮับองค์กร) และอีกสภาพแวดล้อมใช้สำหรับสเกลยูนิตและมี "ข้อมูลว่างเปล่า"

คุณต้องได้รับ Add-in ของสเกลยูนิตในระบบคลาวด์และแบบปลายทางอย่างน้อยหนึ่งรายการ จากนั้นจะได้รับช่องโครงการและสภาพแวดล้อมที่สอดคล้องกันใน [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) เพื่อให้สภาพแวดล้อมสเกลยูนิตสามารถปรับใช้ได้โดยใช้ [พอร์ทัล Scale Unit Manager](https://aka.ms/SCMSUM)

ติดต่อฝ่ายสนับสนุนของ Microsoft เพื่อขอให้เปิดใช้งานสภาพแวดล้อม sandbox

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
