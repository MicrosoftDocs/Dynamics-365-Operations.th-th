---
title: ระบุสมมติฐานและกำหนดตัวชี้วัดสำหรับการทดสอบ
description: หัวข้อนี้อธิบายวิธีการระบุสมมติฐานและตัวชี้วัดความสำเร็จสำหรับการทดลองที่คุณจะทำงานบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 43358264a2107fb139c00ce617054be16a74f935
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/22/2020
ms.locfileid: "4416266"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="cb78a-103">ระบุสมมติฐานและกำหนดตัวชี้วัดความสำเร็จสำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="cb78a-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="cb78a-104">ระยะแรกในวงจรการทดสอบรวมถึงการระบุสมมติฐานสำหรับการทดสอบ และการกำหนดตัวชี้วัดที่คุณจะติดตามเพื่อประเมินความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="cb78a-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="cb78a-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับ [การตั้งค่าและการรันการทดลอง](experimentation-overview.md) บนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cb78a-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cb78a-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="cb78a-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="cb78a-107">[ ![การเดินทางของผู้การทดสอบใช้ - ระบุ](./media/experimentation_identify.svg)](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cb78a-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="cb78a-108">สมมติฐานคือคำชี้แจงที่คุณคาดการณ์ถึงผลลัพธ์ของการทดลอง</span><span class="sxs-lookup"><span data-stu-id="cb78a-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="cb78a-109">หลายปัจจัยใช้กำหนดสมมติฐาน ตัวอย่างเช่น การวิจัยเกี่ยวกับพฤติกรรมของผู้ใช้ และข้อมูลเว็บไซต์ที่คุณรวบรวมไว้</span><span class="sxs-lookup"><span data-stu-id="cb78a-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="cb78a-110">ด้วยสมมติฐาน คุณจะกำหนดสมมติฐานหรือทฤษฎีที่คุณต้องการตรวจสอบความถูกต้องด้วยการทดลองของคุณ</span><span class="sxs-lookup"><span data-stu-id="cb78a-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="cb78a-111">ตัวอย่างของสมมติฐานสำหรับการทดลองของคุณอาจเป็น "*ภาพของเสื้อยืดสีขาวบนโฮมเพจของฉันจะขับเคลื่อนอัตราการคลิกที่สูงกว่าเสื้อกันหนาวสีน้ำเงินในช่วงเดือนฤดูร้อน เพราะคนต้องการที่จะสวมใส่สิ่งที่มีน้ำหนักเบาและสีอ่อนในช่วงฤดูร้อน*"</span><span class="sxs-lookup"><span data-stu-id="cb78a-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="cb78a-112">ในกรณีดังกล่าว คุณจะสร้างการเปลี่ยนแปลงที่รวมเสื้อยืดสีขาวและเสื้อกันหนาวสีน้ำเงิน และเผยแพร่ทั้งสองอย่างในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cb78a-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="cb78a-113">เมื่อต้องการตรวจสอบสมมติฐาน ความสำเร็จหรือความล้มเหลวของการทดลองควรเชื่อมโยงกับการดำเนินการของผู้ใช้โดยตรง ตัวอย่างเช่น ถ้าผู้ใช้เว็บไซต์คลิกลิงค์หรือปุ่ม</span><span class="sxs-lookup"><span data-stu-id="cb78a-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="cb78a-114">การดำเนินการเหล่านี้ต้องตรงกับเหตุการณ์ที่จะรายงานไปยังบริการของบุคคลที่สามที่ติดตามการทดลอง</span><span class="sxs-lookup"><span data-stu-id="cb78a-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="cb78a-115">เมื่อเวลาผ่านไป เปอร์เซ็นต์ของผู้ใช้ที่ทำการดำเนินการจะใช้เป็นตัวชี้วัดที่คุณสามารถใช้ในการสร้างรายงานและดำเนินการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="cb78a-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="cb78a-116">เพื่อตรวจทานเหตุการณ์และแอททริบิวต์ที่พร้อมใช้งานทั้งหมด ดูที่ [เหตุการณ์ส่วนประกอบ Commerce สำหรับการวินิจฉัยและการแก้ไขปัญหา](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="cb78a-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="cb78a-117">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="cb78a-117">Previous step</span></span>
[<span data-ttu-id="cb78a-118">การทดสอบใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cb78a-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="cb78a-119">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="cb78a-119">Next step</span></span>
[<span data-ttu-id="cb78a-120">การตั้งค่าการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="cb78a-120">Set up an experiment</span></span>](experimentation-setup.md)
