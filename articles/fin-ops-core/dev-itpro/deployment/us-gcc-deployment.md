---
title: Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ใน US Government Community Cloud (GCC)
description: หัวข้อนี้มีข้อมูลเกี่ยวกับผลิตภัณฑ์ Microsoft Dynamics 365 US Government ซึ่งสามารถใช้งานเฉพาะกับหน่วยงานรัฐบาลและเอกชนที่เข้าเกณฑ์
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 17702ada5bf75a44652e194c2555a83e76e7a36b
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817451"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ใน US Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

เลือกผลิตภัณฑ์ Microsoft Dynamics 365 United States (US) Government ที่สามารถใช้งานกับหน่วยงานรัฐบาลและเอกชนที่เข้าเกณฑ์ หน่วยงานดังกล่าวจํากัดเฉพาะชนิดต่อไปนี้

- รัฐบาลกลางสหรัฐฯ รัฐ ท้องถิ่น ชนเผ่า และหน่วยงานราชการของแต่ละประเทศ
- หน่วยงานเอกชนที่ใช้ Dynamics 365 US Government เพื่อให้บริการโซลูชันแก่หน่วยงานราชการหรือสมาชิกของชุมชนระบบคลาวด์ที่เข้าเกณฑ์
- หน่วยงานเอกชนที่มีข้อมูลลูกค้าซึ่งอยู่ภายใต้ข้อบังคับของรัฐบาล และ Dynamics 365 US Government เป็นบริการที่เหมาะสมเพื่อตอบสนองความต้องการด้านระเบียบบังคับ

สำหรับข้อมูล โปรดดูที่ [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)

## <a name="onboarding"></a>การเตรียมความพร้อม

หากต้องการดําเนินการเตรียมความพร้อมครั้งแรกสำหรับโครงการการใช้งานใน Microsoft Dynamics Lifecycle Services (LCS) ให้ปฏิบัติตามคําแนะนํา [เตรียมความพร้อมสำหรับโครงการการใช้งาน](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). อย่างไรก็ตาม อย่าใช้ลิงก์กับ LCS สาธารณะที่ให้ไว้ในคําแนะนําเหล่านั้น แต่ให้ใช้ URL ต่อไปนี้เพื่อเปิด LCS สำหรับ US Government Community Cloud (GCC): <https://gov.lcs.microsoftdynamics.us>

หลังจากการเตรียมความพร้อมครั้งแรกเสร็จสมบูรณ์ ให้ปฏิบัติตามคําแนะนำใน [การเตรียมความพร้อมของโครงการ](../lifecycle-services/project-onboarding.md) ขอย้ำว่าให้ใช้ [LCS สำหรับ GCC](https://gov.lcs.microsoftdynamics.us) แทน LCS สาธารณะ

## <a name="environment-deployment"></a>การปรับใช้งานสภาพแวดล้อม

หลังจากที่คุณได้เสร็จสิ้นการเตรียมความพร้อมของโครงการแล้ว คุณสามารถทบทวนความสามารถเพิ่มเติมของ LCS ที่อธิบายไว้ใน [Lifecycle Services (LCS) สำหรับลูกค้าที่ใช้แอป Finance and Operations](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) จากนั้นย้ายไปยังการปรับใช้งานสภาพแวดล้อม

- หากต้องการปรับใช้งานสภาพแวดล้อมที่มีการจัดการโดย Microsoft ผ่าน LCS ให้ปฏิบัติตามคําแนะนําใน [Lifecycle Services (LCS) สำหรับลูกค้าที่ใช้แอป Finance and Operations](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience)
- สำหรับสภาพแวดล้อมที่โฮสต์ในระบบคลาวด์ ดูที่ [ปรับใช้งานและเข้าถึงสภาพแวดล้อมการพัฒนา](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) คุณต้องทำกระบวนการเตรียมความพร้อมของ Resource Manager ให้กับตัวเชื่อมต่อของคุณให้เสร็จสมบูรณ์ตามที่อธิบายไว้ใน [ทำกระบวนการเตรียมความพร้อมของ Azure Resource Manager สำหรับโครงการ US Government Lifecycle Services ให้เสร็จสมบูรณ์](arm-onbarding-us-goverment.md)

> [!NOTE]
> สำหรับโครงการ US Government LCS รองรับการสมัครใช้งาน Azure เฉพาะ Azure Government เท่านั้น

## <a name="features-that-arent-available"></a>คุณลักษณะที่ไม่พร้อมให้ใช้งาน

คุณลักษณะบางอย่างจะไม่สามารถใช้ได้กับการปรับใช้งานใน GCC หรือคุณลักษณะเหล่านั้นจะไม่สามารถใช้ได้กับ Dynamics 365 ใน GCC ตัวอย่างเช่น บริการ Azure DevOps จะไม่สามารถใช้ได้ใน GCC อย่างไรก็ตาม คุณสามารถใช้บริการ Azure DevOps แบบในสถานที่หรือ Azure DevOps สาธารณะได้ สำหรับข้อมูลรายละเอียดของความพร้อมใช้งานของคุณลักษณะ ดูที่ [ความพร้อมใช้งานของคุณลักษณะ Business Applications US Government](https://aka.ms/BAPFunctionalParity)

## <a name="frequently-asked-questions"></a>คำถามที่ถามบ่อย

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Dynamics 365 Finance และ Dynamics 365 Supply Chain Management รองรับใน GCC-High หรือไม่

ไม่ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management รองรับเฉพาะใน GCC เท่านั้น

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>ฉันสามารถใช้ Azure DevOps สาธารณะกับ Finance และ Supply Chain Management ใน GCC ได้หรือไม่

ได้ คุณสามารถใช้บริการ Azure DevOps สาธารณะได้หากคุณไม่ได้มีข้อจํากัดของโซลูชันที่ได้รับการรับรองโดย Federal Risk and Authorization Management Program (FEDRAMP) หรือคุณสามารถใช้ Azure DevOps Server ก็ได้

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>ฉันจะสามารถปรับใช้งานสภาพแวดล้อมการพัฒนาที่เป็นสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์ระดับ 1 ในการสมัครใช้งาน Azure Commercial ได้หรือไม่

ไม่ ใน [LCS สำหรับ GCC](https://gov.lcs.microsoftdynamics.us) คุณต้องใช้การสมัครใช้งาน Azure Government ในการปรับใช้งานสภาพแวดล้อมที่โฮสต์บนระบบคลาวด์

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>ฉันต้องทำอย่างไรหากฉันต้องใช้แพคเกจจากไลบรารีแอสเซทที่ใช้ร่วมกัน แต่ไม่มีอยู่ใน LCS สำหรับ GCC

คุณสามารถดาวน์โหลดแพคเกจเดียวกันจากไลบรารีแอสเซทที่ใช้ร่วมกันใน [LCS สาธารณะ](https://lcs.dynamics.com) หรือคู่ค้าของคุณสามารถช่วยคุณดาวน์โหลดแพคเกจได้

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>เครื่องมือปรับรุ่นโค้ดสามารถใช้ได้ใน GCC หรือไม่

ไม่ เครื่องมือปรับรุ่นโค้ดยังไม่สามารถใช้ได้ใน GCC แต่คุณสามารถสร้างโครงการผู้ที่มีแนวโน้มจะเป็นลูกค้าใน [LCS สาธารณะ](https://lcs.dynamics.com) และใช้เครื่องมือปรับรุ่นโค้ด โปรดทราบว่าคุณจะไม่สามารถปรับใช้งานสภาพแวดล้อมในโครงการผู้ที่มีแนวโน้มจะเป็นลูกค้าได้

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>คู่ค้าสามารถเปิดตั๋วการสนับสนุนในนามของฉันได้หรือไม่

ใช่ แต่หากคู่ค้าของคุณใช้ข้อมูลเฉพาะตัวที่ไม่ใช่ GCC ตั๋วการสนับสนุนจะได้รับการส่งไปยังคิวการสนับสนุนสาธารณะ เราขอแนะนำให้คุณใช้การให้สิทธิ์ GCC ของลูกค้าใน LCS เพื่อเปิดตั๋วการสนับสนุน

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [ความพร้อมใช้งานของคุณลักษณะ Business Applications US Government](https://aka.ms/BAPFunctionalParity)
- [คู่มือผู้ใช้ Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [ภาพรวมของการปรับใช้ระบบคลาวด์](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
