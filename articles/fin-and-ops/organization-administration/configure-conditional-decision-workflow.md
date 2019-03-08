---
title: ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน
description: ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับการตัดสินใจแบบมีเงื่อนไข
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01290b3e2810aa1762f2230e8d01d219d6b10bf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "328205"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="bcb26-103">ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bcb26-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcb26-104">ใช้กระบวนงานต่อไปนี้เพื่อตั้งค่าคอนฟิกคุณสมบัติสำหรับการตัดสินใจแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bcb26-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="bcb26-105">การตัดสินใจแบบมีเงื่อนไขเป็นจุดที่ลำดับงานแบ่งออกเป็นสองสาขา </span><span class="sxs-lookup"><span data-stu-id="bcb26-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="bcb26-106">หากต้องการตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในโปรแกรมแก้ไขลำดับงาน ให้คลิกขวาที่การตัดสินใจแบบมีเงื่อนไขนั้น แล้วคลิก **คุณสมบัติ** เพื่อเปิดแบบฟอร์ม **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="bcb26-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="bcb26-107">กำหนดชื่อการตัดสินใจ</span><span class="sxs-lookup"><span data-stu-id="bcb26-107">Name a decision</span></span>

<span data-ttu-id="bcb26-108">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับการตัดสินใจแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bcb26-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="bcb26-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="bcb26-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="bcb26-110">ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับการตัดสินใจแบบมีเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bcb26-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="bcb26-111"> กำหนดเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bcb26-111">Set conditions</span></span>

<span data-ttu-id="bcb26-112">ระบบกำหนดว่าจะใช้สาขาใดโดยการประเมินเอกสารที่ส่งเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่ระบุหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bcb26-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="bcb26-113">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="bcb26-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="bcb26-114">คลิก **เพิ่มเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="bcb26-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="bcb26-115">ป้อนเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="bcb26-115">Enter a condition.</span></span>
4. <span data-ttu-id="bcb26-116">ป้อนเงื่อนไขเพิ่มเติมถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="bcb26-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="bcb26-117">หากต้องการตรวจสอบว่าเงื่อนไขที่คุณป้อนเข้าไปตั้งค่าคอนฟิกไว้ถูกต้องหรือไม่ ให้ทำตามขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="bcb26-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="bcb26-118">คลิก **ทดสอบ** เพื่อเปิดแบบฟอร์ม **ทดสอบเงื่อนไขลำดับงาน**</span><span class="sxs-lookup"><span data-stu-id="bcb26-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="bcb26-119">เลือกเรกคอร์ดในพื้นที่ของแบบฟอร์ม **ตรวจสอบเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="bcb26-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="bcb26-120">คลิก **ทดสอบ**</span><span class="sxs-lookup"><span data-stu-id="bcb26-120">Click **Test**.</span></span> <span data-ttu-id="bcb26-121">ระบบจะประเมินเรกคอร์ดเพื่อพิจารณาว่าเป็นไปตามเงื่อนไขที่คุณกำหนดไว้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="bcb26-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="bcb26-122">คลิก **ตกลง** หรือ **ยกเลิก** เพื่อกลับไปที่แบบฟอร์ม **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="bcb26-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>
