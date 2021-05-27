---
title: การแจ้งเตือนการดำเนินการเวฟ
description: หัวข้อนี้จะอธิบายการแจ้งเตือนการดำเนินเวฟ และอธิบายวิธีการตั้งค่า
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019165"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="80391-103">การแจ้งเตือนการดำเนินการเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="80391-104">คุณลักษณะ *การแจ้งเตือนการดำเนินการเวฟ* ใช้เหตุการณ์ทางธุรกิจและศูนย์การดำเนินการเพื่อจัดส่งการแจ้งเตือนที่เกี่ยวข้องกับการดำเนินการเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="80391-105">ซึ่งช่วยให้คุณสามารถระบุชนิดของเหตุการณ์ที่สร้างการแจ้งเตือน คลังสินค้าที่สร้างการแจ้งเตือน และผู้ใช้ที่รับสินค้านั้น</span><span class="sxs-lookup"><span data-stu-id="80391-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="80391-106">ปุ่ม **แสดงข้อความ** (สัญลักษณ์ข้อความ) บนด้านขวาของแถบนําทางบ่งชี้ว่าข้อความศูนย์การดำเนินการพร้อมใช้งานเมื่อใดของผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="80391-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="80391-107">ผู้ใช้สามารถเลือกปุ่ม **แสดงข้อความ** เพื่อเปิดศูนย์การดำเนินการและตรวจทานข้อความได้</span><span class="sxs-lookup"><span data-stu-id="80391-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="80391-108">เหตุการณ์ทางธุรกิจเกิดขึ้นเมื่อรันกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="80391-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="80391-109">กระบวนการทางธุรกิจมีภารกิจต่างๆ</span><span class="sxs-lookup"><span data-stu-id="80391-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="80391-110">ในระหว่างกระบวนการทางธุรกิจ ผู้ใช้ที่เข้าร่วมกิจกรรมดังกล่าวจะปฏิบัติการธุรกิจเพื่อปฏิบัติงานเหล่านั้นให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="80391-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="80391-111">เหตุการณ์ทางธุรกิจเป็นระบบที่ปล่อยให้ระบบภายนอกได้รับการแจ้งเตือนจากโปรแกรมประยุกต์ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="80391-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="80391-112">ด้วยวิธีนี้ ระบบจะสามารถปฏิบัติงานทางธุรกิจเพื่อตอบสนองต่อเหตุการณ์ทางธุรกิจได้</span><span class="sxs-lookup"><span data-stu-id="80391-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="80391-113">สำหรับข้อมูลเพิ่มเติม ให้ดู [ภาพรวมเหตุการณ์ทางธุรกิจ](../../fin-ops-core/dev-itpro/business-events/home-page.md)</span><span class="sxs-lookup"><span data-stu-id="80391-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="80391-114">เปิดคุณลักษณะการแจ้งเตือนการดำเนินการเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="80391-115">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การแจ้งเตือนการดำเนินการเวฟ* ต้องมีการเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="80391-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="80391-116">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="80391-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="80391-117">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80391-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="80391-118">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="80391-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="80391-119">**ชื่อคุณลักษณะ:** *เปิดการแจ้งเตือนการดำเนินการเวฟ*</span><span class="sxs-lookup"><span data-stu-id="80391-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="80391-120">สถานการณ์: ส่งการแจ้งเตือนการดำเนินการชุดงานเวฟไปยังศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="80391-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="80391-121">สถานการณ์นี้แสดงโฟลว์สิ้นสุดของการส่งการแจ้งเตือนเกี่ยวกับข้อผิดพลาดการรันชุดงานเวฟไปยังบทบาทเฉพาะผ่านทางศูนย์การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="80391-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="80391-122">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="80391-122">Make demo data available</span></span>

<span data-ttu-id="80391-123">เพื่อติดตามสถานการณ์จำลองนี้ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="80391-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="80391-124">ตรวจสอบให้แน่ใจว่าเวฟรันในโหมดชุดงาน</span><span class="sxs-lookup"><span data-stu-id="80391-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="80391-125">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> พารามิเตอร์การจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="80391-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="80391-126">บนแท็บด่วน **การประมวลผลเวฟ** ให้ตั้งค่าตัวเลือก **การประมวลผลเวฟในชุดงาน** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="80391-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="80391-127">หากคุณต้องการปิดใช้งานการแจ้งเตือนการรันชุดงานของเวฟ ให้ตั้งค่าตัวเลือก **ปิดใช้งานการแจ้งเตือนชุดงานการประมวลผลเวฟ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="80391-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="80391-128">ตั้งค่าคอนฟิกนโยบายการแจ้งเตือนเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-128">Configure a wave notification policy</span></span>

<span data-ttu-id="80391-129">นโยบายการแจ้งเตือนเวฟกําหนดชนิดของการแจ้งเตือนที่ส่งและผู้ใช้ที่ได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="80391-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="80391-130">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> นโยบายการแจ้งเตือนเวฟ**</span><span class="sxs-lookup"><span data-stu-id="80391-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="80391-131">สร้างเรกคอร์ดที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80391-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="80391-132">**นโยบายการแจ้งเตือนเวฟ:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="80391-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="80391-133">**คำอธิบาย:** *ข้อผิดพลาดชุดงานเวฟ 24 ของคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="80391-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="80391-134">**ส่งการแจ้งเตือนเมื่อ:** *ข้อผิดพลาดอย่างเดียว*</span><span class="sxs-lookup"><span data-stu-id="80391-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="80391-135">**บทบาท:** *ผู้ดูแลระบบ*</span><span class="sxs-lookup"><span data-stu-id="80391-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="80391-136">เนื่องจากสถานการณ์นี้ใช้ข้อมูลสาธิต มีการเลือกบทบาท *ผู้ดูแลระบบ* เพื่อความง่ายในการทำงาน</span><span class="sxs-lookup"><span data-stu-id="80391-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="80391-137">ดังนั้น เนื่องจากคุณเข้าสู่ระบบในฐานะผู้ใช้ของผู้ดูแลระบบ คุณจะได้รับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="80391-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="80391-138">อย่างไรก็ตาม ในทางปฏิบัติ คุณควรเลือกบทบาทที่เฉพาะเจาะจงมากขึ้นเพื่อแจ้งให้ทราบเกี่ยวกับข้อผิดพลาดการรันชุดงานเวฟ เช่น *ผู้จัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="80391-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="80391-139">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="80391-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="80391-140">ตั้งค่าคอนฟิกเท็มเพลตเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-140">Configure a wave template</span></span>

<span data-ttu-id="80391-141">เท็มเพลตเวฟช่วยให้คุณสามารถเชื่อมโยงอินสแตนซ์ที่เฉพาะเจาะจงของวิธีการเวฟไปยังแม่แบบป้ายชื่อเวฟที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="80391-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="80391-142">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="80391-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="80391-143">ในบานหน้าต่างรายการ ให้ตั้งค่าฟิลด์ **ชนิดของแม่แบบเวฟ** เป็น *การจัดส่ง* แล้วเลือกแม่แบบเวฟ *ค่าเริ่มต้นของการจัดส่ง 24* ในคลังสินค้า 24</span><span class="sxs-lookup"><span data-stu-id="80391-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="80391-144">บน FastTab **ทั่วไป** ให้ตั้งค่าฟิลด์ **นโยบายการแจ้งเตือนเวฟ** เป็น *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="80391-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="80391-145">ตั้งค่าคอนฟิกแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="80391-145">Configure a work template</span></span>

<span data-ttu-id="80391-146">แม่แบบงานมีการใช้ในระหว่างการประมวลผลเวฟเพื่อสร้างงาน</span><span class="sxs-lookup"><span data-stu-id="80391-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="80391-147">สำหรับสถานการณ์นี้ การดำเนินการเวฟควรทริกเกอร์ข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="80391-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="80391-148">โดยการตั้งค่าการสอบถามแม่แบบงานเพื่อใช้คลังสินค้าที่ไม่มีอยู่ คุณจะตรวจสอบให้แน่ใจว่าการดำเนินการเวฟล้มเหลวและส่งการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="80391-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="80391-149">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="80391-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="80391-150">ในบานหน้าต่างรายการ ให้ตั้งค่าฟิลด์ **ชนิดของแม่แบบงาน** เป็น *ใบสั่งขาย* แล้วเลือกแม่แบบงาน *24 SO Stage* ในคลังสินค้า 24</span><span class="sxs-lookup"><span data-stu-id="80391-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="80391-151">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="80391-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="80391-152">ในกล่องโต้ตอบโปรแกรมแก้ไขการสอบถาม บนแท็บ **ช่วง** ให้แก้ไขแถวต่อไปนี้ (หรือเพิ่มแถวถ้าไม่มีอยู่):</span><span class="sxs-lookup"><span data-stu-id="80391-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="80391-153">**ตาราง:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="80391-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="80391-154">**ตารางที่ได้รับมา:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="80391-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="80391-155">**ฟิลด์:** *คลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="80391-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="80391-156">**เกณฑ์:** เปลี่ยนค่าจาก *24* เป็น *ข้อผิดพลาด*</span><span class="sxs-lookup"><span data-stu-id="80391-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="80391-157">เลือก **ตกลง** และยืนยันรายละเอียดการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="80391-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="80391-158">สร้างใบสั่งขายและนำใบสั่งขายออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="80391-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="80391-159">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="80391-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="80391-160">สร้างใบสั่งขายที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80391-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="80391-161">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="80391-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="80391-162">**คลังสินค้า:** *24*</span><span class="sxs-lookup"><span data-stu-id="80391-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="80391-163">บนแท็บด่วน **รายการใบสั่งขาย** ให้เพิ่มบรรทัดใบสั่งขายที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="80391-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="80391-164">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="80391-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="80391-165">**ปริมาณ:** *10*</span><span class="sxs-lookup"><span data-stu-id="80391-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="80391-166">สินค้าและปริมาณเหล่านี้เป็นเพียงตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="80391-166">These items and quantities are only examples.</span></span> <span data-ttu-id="80391-167">คลังสินค้าที่ระบุต้องมีสินค้าคงคลังเพียงพอ</span><span class="sxs-lookup"><span data-stu-id="80391-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="80391-168">ในขณะที่รายการใบสั่งใหม่ยังคงถูกเลือกอยู่บนแท็บด่วน **รายการใบสั่งขาย** ให้เลือก **สินค้าคงคลัง \> การจอง** บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="80391-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="80391-169">บนหน้า **การจองสินค้า** บนบานหน้าต่างการดำเนินการ ให้เลือก **จองล็อต**</span><span class="sxs-lookup"><span data-stu-id="80391-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="80391-170">จากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="80391-170">Then close the page.</span></span>
1. <span data-ttu-id="80391-171">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="80391-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="80391-172">การแจ้งเตือนจากการดำเนินงานชุดงานเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="80391-173">คุณจะได้รับการแจ้งเตือนเกี่ยวกับการดำเนินงานเวฟล้มเหลวโดยขึ้นอยู่กับการตั้งค่าเหตุการณ์ทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="80391-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="80391-174">ข้อความของศูนย์การดำเนินงานจะคล้ายกับตัวอย่างต่อไปนี้ และจะรวมลิงค์ไปที่เวฟที่ล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="80391-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="80391-175">**เกิดข้อผิดพลาดระหว่างการดำเนินการเวฟ**</span><span class="sxs-lookup"><span data-stu-id="80391-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="80391-176">เกิดข้อผิดพลาดขณะรันเวฟ USMF-000000001 โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="80391-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="80391-177">ข้อความล่าสุด: ไม่มีการสร้างงานใดสำหรับเวฟ USMF-000000001</span><span class="sxs-lookup"><span data-stu-id="80391-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="80391-178">**สถานะ**</span><span class="sxs-lookup"><span data-stu-id="80391-178">**STATUS**</span></span>  
> <span data-ttu-id="80391-179">ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="80391-179">Active</span></span>
>
> <span data-ttu-id="80391-180">เปิดรายละเอียดเวฟ</span><span class="sxs-lookup"><span data-stu-id="80391-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
