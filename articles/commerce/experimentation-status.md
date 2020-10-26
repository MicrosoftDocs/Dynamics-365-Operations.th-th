---
title: ตรวจสอบสถานะของการทดสอบ
description: หัวข้อนี้อธิบายสถานะของการทดลองในวงจรการทดสอบใน Dynamics 365 Commerce
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930297"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="ea5da-103">ตรวจสอบสถานะของการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="ea5da-103">Review the status of an experiment</span></span>
<span data-ttu-id="ea5da-104">มีขั้นตอนหลายอย่างที่เกี่ยวข้องกับการตั้งค่าและการรันการทดลองใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ea5da-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ea5da-105">สำหรับข้อมูลเกี่ยวกับขั้นตอนวงจรการทดสอบ ให้ดูที่ [การทดสอบใน Dynamics 365 Commerce](experimentation-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ea5da-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="ea5da-106">เมื่อต้องการเรียนรู้ว่าการทดลองอยู่ตรงไหนในวงจรการใช้งาน ไปที่แท็บ **การทดลอง** ในโปรแกรมสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="ea5da-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="ea5da-107">รายการของการทดลองจะแสดงขึ้นพร้อมกับสถานะของการทดลองแต่ละอย่างในทั้ง Commerce และบริการของบุคคลที่สามที่ใช้ เพื่อเปิดใช้งานการสร้างการทดลอง กำหนดความแตกต่าง และวิเคราะห์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ea5da-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="ea5da-108">ในคอลัมน์ **สถานะ Commerce** อาจแสดงค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ea5da-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="ea5da-109">**แบบร่าง** - การทดลองเชื่อมโยงกับหน้าหรือส่วนใน Commerce และกำลังแก้ไข</span><span class="sxs-lookup"><span data-stu-id="ea5da-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="ea5da-110">**เผยแพร่** - ความแตกต่างของการทดลองพร้อมที่จะแสดงบนเว็บไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="ea5da-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="ea5da-111">ถ้าการทดสอบกำลังรันอยู่ในบริการของบุคคลที่สาม ผู้ใช้เว็บไซต์จะเห็นความเปลี่ยงแปลงของหน้าหรือส่วนที่เลือกโดยบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="ea5da-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="ea5da-112">**ไม่ได้เผยแพร่** - การทดลองไม่มีอยู่บนเว็บไซต์ของคุณอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="ea5da-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="ea5da-113">ผู้ใช้เว็บไซต์จะเห็นความเปลี่ยงแปลงของหน้าหรือส่วนที่เลือกโดยบริการของบุคคลที่สาม แม้ว่าการทดสอบกำลังรันอยู่ในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="ea5da-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="ea5da-114">**เสร็จสมบูรณ์** - การทดลองทำงานตามหลักสูตร และมีการเลื่อนระดับเปลี่ยนแปลงเป็นใช้งานจริงให้กับผู้ใช้เว็บไซต์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="ea5da-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="ea5da-115">ในลักษณะเดียวกัน ในคอลัมน์ **สถานะของบุคคลที่สาม** อาจแสดงค่าต่อไปนี้เพื่อบ่งชี้ว่าสถานะใดที่การทดลองอยู่ในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="ea5da-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="ea5da-116">**แบบร่าง** - การทดลองถูกตั้งค่าในบริการของบุคคลที่สาม แต่ยังไม่ได้เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ea5da-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="ea5da-117">**กำลังรัน** - การทดลองเริ่มต้นแล้วในบริการของบุคคลที่สาม และกำลังรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ea5da-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="ea5da-118">**หยุดชั่วคราว** - การทดลองถูกหยุดชั่วคราว และไม่มีการรวบรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ea5da-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="ea5da-119">คุณต้องดำเนินการทดลอง เพื่อรวบรวมข้อมูลอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="ea5da-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="ea5da-120">**ที่เก็บถาวร** - การทดลองทำงานหลักสูตร และได้รับการเก็บในบริการของบุคคลที่สามสำหรับการอ้างอิงในอนาคต</span><span class="sxs-lookup"><span data-stu-id="ea5da-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="ea5da-121">แผนภาพด้านล่างจะแสดงสถานะทั้งสองชุด และวิธีที่เกี่ยวข้องกับแต่ละชุด</span><span class="sxs-lookup"><span data-stu-id="ea5da-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="ea5da-122">[ ![สถานะการทดสอบ](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ea5da-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
