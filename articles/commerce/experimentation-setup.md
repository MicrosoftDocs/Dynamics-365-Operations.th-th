---
title: การตั้งค่าการทดสอบ
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการทดลองในบริการของบุคคลที่สาม
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dfd7b8cb13f4d69811b5a86b971fa1b57c75bd36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234620"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="55576-103">การตั้งค่าการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="55576-103">Set up an experiment</span></span>

<span data-ttu-id="55576-104">หลังจากที่คุณ [กำหนดสมมติฐานและกำหนดการวัดความสำเร็จใดที่คุณต้องการใช้](experimentation-identify.md) คุณจะต้องตั้งค่าการทดลองของคุณในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="55576-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="55576-105">แผนภาพต่อไปนี้แสดงขั้นตอนทั้งหมดที่เกี่ยวข้องกับการตั้งค่า และการรันการทดลองบนเว็บไซต์อีคอมเมิร์ซใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="55576-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="55576-106">ขั้นตอนเพิ่มเติมครอบคลุมอยู่ในหัวข้อที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="55576-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="55576-107">[ ![การเดินทางของผู้การทดสอบใช้ - การตั้งค่า](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="55576-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="55576-108">ตั้งค่าการทดลองของคุณในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="55576-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="55576-109">ขณะนี้คุณควรเลือกบริการของบุคคลที่สามเพื่อรันและตรวจสอบการทดลองของคุณ และตั้งค่าตัวเชื่อมต่อการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="55576-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="55576-110">ข้อกำหนดเบื้องต้นเหล่านี้จะแสดงรายการอยู่ใน  [การทดสอบใน Dynamics 365 Commerce](experimentation-overview.md)</span><span class="sxs-lookup"><span data-stu-id="55576-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="55576-111">ทำตามขั้นตอนที่จำเป็นในการสร้างการทดลองของคุณในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="55576-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="55576-112">ถ้ามีการตั้งค่าคอนฟิกตัวเชื่อมต่ออย่างถูกต้อง รายการที่สมบูรณ์ของการทดลองที่คุณตั้งค่าไว้ในบริการของบุคคลที่สามจะแสดงในตัวสร้างไซต์ Commerce ภายในประมาณ 5 นาที</span><span class="sxs-lookup"><span data-stu-id="55576-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="55576-113">ตั้งค่าตัวชี้วัดความสำเร็จของคุณ</span><span class="sxs-lookup"><span data-stu-id="55576-113">Set up your success metrics</span></span>
<span data-ttu-id="55576-114">การทดสอบทั้งหมดต้องมีตัวชี้วัดที่จะวัดผลของการเปลี่ยนแปลง และตรวจสอบความถูกต้องของสมมติฐาน</span><span class="sxs-lookup"><span data-stu-id="55576-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="55576-115">ให้ทำตามขั้นตอนต่อไปนี้เพื่อเปิดใช้งานการคำนวณตัวชี้วัดในบริการของบุคคลที่สามโดยใช้เหตุการณ์ การตรวจวัดระยะไกลแบบใช้งานจริงจาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="55576-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="55576-116">หากต้องการตั้งค่าตัวชี้วัดความสำเร็จ ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55576-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="55576-117">ในโปรแกรมสร้างไซต์ Commerce ให้เลือกแท็บ **หน้า** ในบานหน้าต่างนำทางด้านซ้าย แล้วเลือกหน้าที่คุณต้องการรวบรวมตัวชี้วัด</span><span class="sxs-lookup"><span data-stu-id="55576-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="55576-118">ไปที่ส่วน **รหัสเหตุการณ์เพื่อติดตาม** ในบานหน้าต่างคุณสมบัติด้านขวาของหน้าหรือโมดูลที่คุณต้องการติดตาม</span><span class="sxs-lookup"><span data-stu-id="55576-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="55576-119">เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="55576-119">Select **View**.</span></span> <span data-ttu-id="55576-120">รายการของรหัสเหตุการณ์ทั้งหมดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="55576-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="55576-121">คัดลอกเหตุการณ์ที่คุณต้องการติดตาม และวางคีย์เหตุการณ์ลงในสถานที่ที่กำหนดไว้ในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="55576-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="55576-122">ถ้าคุณต้องการมากกว่าหนึ่งเหตุการณ์ ให้คัดลอกคีย์ทีละครั้ง</span><span class="sxs-lookup"><span data-stu-id="55576-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="55576-123">เมื่อต้องการเรียนรู้วิธีดูเหตุการณ์และแอททริบิวต์ทั้งหมดที่พร้อมใช้งาน รวมทั้งมุมมองหน้าและการติดตามรายได้ โปรดดู [เหตุการณ์ส่วนประกอบ Commerce สำหรับการวินิจฉัยและการแก้ไขปัญหา](dev-itpro/retail-component-events-diagnostics-troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="55576-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="55576-124">ดำเนินการขั้นตอนอื่นๆ สำหรับการติดตามตัวชี้วัดตามที่จำเป็นในบริการของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="55576-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="55576-125">ขั้นตอนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="55576-125">Previous step</span></span>
[<span data-ttu-id="55576-126">ระบุสมมติฐานและกำหนดตัวชี้วัดสำหรับการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="55576-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="55576-127">ขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="55576-127">Next step</span></span>
[<span data-ttu-id="55576-128">เชื่อมต่อและแก้ไขการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="55576-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]