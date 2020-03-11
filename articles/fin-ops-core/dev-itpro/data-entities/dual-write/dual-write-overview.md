---
title: ภาพรวมของการรวมแบบสองทิศทาง
description: หัวข้อนี้แสดงภาพรวมของการรวมแบบสองทิศทาง การรวมแบบสองทิศทางเป็นโครงสร้างพื้นฐานที่ให้การโต้ตอบแบบใกล้เรียลไทม์ระหว่างแอปที่เป็นแบบโมเดล Microsoft Dynamics 365 และแอป Finance and Operations
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076005"
---
# <a name="dual-write-overview"></a><span data-ttu-id="a44b7-104">ภาพรวมของการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a44b7-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="a44b7-105">การรวมแบบสองทิศทางคืออะไร</span><span class="sxs-lookup"><span data-stu-id="a44b7-105">What is dual-write?</span></span>

<span data-ttu-id="a44b7-106">การรวมแบบสองทิศทางเป็นโครงสร้างพื้นฐานแบบสำเร็จรูปที่ให้การโต้ตอบแบบใกล้เรียลไทม์ระหว่างแอปที่เป็นแบบโมเดลใน Microsoft Dynamics 365 และแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a44b7-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="a44b7-107">เมื่อข้อมูลเกี่ยวกับลูกค้า ผลิตภัณฑ์ บุคคล และการดำเนินงาน จะทำงานเกินขอบเขตของแอพลิเคชัน แผนกทั้งหมดในองค์กรมีอำนาจ</span><span class="sxs-lookup"><span data-stu-id="a44b7-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="a44b7-108">การรวมแบบสองทิศทางให้การรวมแบบสองทิศทางที่จับคู่กันระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a44b7-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="a44b7-109">การเปลี่ยนแปลงข้อมูลใดๆ ในแอป Finance and Operations ทำให้เกิดการเขียนไปยัง Common Data Service และการเปลี่ยนแปลงข้อมูลใดๆ ใน Common Data Service ทำให้เกิดการเขียนไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a44b7-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="a44b7-110">โฟลว์ข้อมูลโดยอัตโนมัตินี้จะให้ประสบการณ์ผู้ใช้แบบรวมทั่วทั้งแอป</span><span class="sxs-lookup"><span data-stu-id="a44b7-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![ความสัมพันธ์ของข้อมูลระหว่างแอป](media/dual-write-overview.jpg)

<span data-ttu-id="a44b7-112">การรวมแบบสองทิศทางมีสองด้าน: ด้าน *โครงสร้างพื้นฐาน* และ *แอพลิเคชัน*</span><span class="sxs-lookup"><span data-stu-id="a44b7-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="a44b7-113">โครงสร้างพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="a44b7-113">Infrastructure</span></span>

<span data-ttu-id="a44b7-114">โครงสร้างพื้นฐานการรวมแบบสองทิศทางสามารถขยายได้และเชื่อถือได้ และรวมถึงคุณลักษณะที่สำคัญต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a44b7-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="a44b7-115">โฟลว์ข้อมูลแบบซิงโครนัสและแบบสองทิศทางระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="a44b7-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="a44b7-116">การซิงโครไนส์ร่วมกับโหมดเล่น หยุดชั่วคราว และติดตาม เพื่อสนับสนุนระบบในระหว่างโหมดอะซิงโครนัสแบบออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="a44b7-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="a44b7-117">ความสามารถในการซิงค์ข้อมูลเบื้องต้นระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="a44b7-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="a44b7-118">มุมมองรวมของกิจกรรมและล็อกข้อผิดพลาดสำหรับผู้ดูแลข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a44b7-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="a44b7-119">ความสามารถในการตั้งค่าคอนฟิกข้อความแจ้งเตือนและขีดจำกัดแบบกำหนดเอง และเพื่อบอกรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="a44b7-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="a44b7-120">อินเทอร์เฟสผู้ใช้ที่ใช้งานง่าย (UI) สำหรับการกรองข้อมูลและการแปลง</span><span class="sxs-lookup"><span data-stu-id="a44b7-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="a44b7-121">ความสามารถในการตั้งค่าและดูการที่ขึ้นต่อกันกับเอนทิตี้และความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="a44b7-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="a44b7-122">ความสามารถในการขยายสำหรับทั้งเอนทิตี้มาตรฐานและเอนทิตี้แบบกำหนดเองและแผนผัง</span><span class="sxs-lookup"><span data-stu-id="a44b7-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="a44b7-123">การจัดการอายุการใช้งานแอพลิเคชันที่เชื่อถือได้</span><span class="sxs-lookup"><span data-stu-id="a44b7-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="a44b7-124">ประสบการณ์การตั้งค่าแบบสำเร็จรูปสำหรับลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="a44b7-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="a44b7-125">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="a44b7-125">Application</span></span>

<span data-ttu-id="a44b7-126">การรวมแบบสองทิศทางสร้างการแม็ประหว่างแนวคิดในแอป Finance and Operations และแนวคิดในแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a44b7-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="a44b7-127">การรวมนี้สนับสนุนสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a44b7-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="a44b7-128">ข้อมูลหลักของลูกค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a44b7-128">Integrated customer master</span></span>
+ <span data-ttu-id="a44b7-129">การเข้าถึงบัตรสมาชิกของลูกค้าและคะแนนรางวัล</span><span class="sxs-lookup"><span data-stu-id="a44b7-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="a44b7-130">ประสบการณ์ใช้งานผลิตภัณฑ์หลักแบบครบวงจร</span><span class="sxs-lookup"><span data-stu-id="a44b7-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="a44b7-131">การรับรู้ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a44b7-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="a44b7-132">ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a44b7-132">Integrated vendor master</span></span>
+ <span data-ttu-id="a44b7-133">การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="a44b7-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="a44b7-134">ประสบการณ์ของกลไกจัดการราคาตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="a44b7-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="a44b7-135">ประสบการณ์ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a44b7-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="a44b7-136">ความสามารถในการให้บริการทั้งสินทรัพย์ภายในองค์กรและสินทรัพย์ของลูกค้าผ่านตัวแทนของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a44b7-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="a44b7-137">ประสบการณ์การสั่งซื้อจนถึงการได้รับเงินสดแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a44b7-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="a44b7-138">กิจกรรมและบันทึกย่อแบบรวมสำหรับข้อมูลลูกค้าและเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a44b7-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="a44b7-139">ความสามารถในการค้นหาความพร้อมของสินค้าคงคลังคงเหลือและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="a44b7-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="a44b7-140">ความสามารถโครงการจนถึงการได้รับเงินสด</span><span class="sxs-lookup"><span data-stu-id="a44b7-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="a44b7-141">ความสามารถในการจัดการที่อยู่และบทบาทต่างๆ ผ่านแนวคิดของฝ่าย</span><span class="sxs-lookup"><span data-stu-id="a44b7-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="a44b7-142">การจัดการแหล่งข้อมูลเดียวสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a44b7-142">Single source management for users</span></span>
+ <span data-ttu-id="a44b7-143">ช่องทางแบบรวมสำหรับการค้าปลีกและการตลาด</span><span class="sxs-lookup"><span data-stu-id="a44b7-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="a44b7-144">การมองเห็นในโปรโมชันและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="a44b7-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="a44b7-145">ฟังก์ชันร้องขอการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="a44b7-145">Request-for-service functions</span></span>
+ <span data-ttu-id="a44b7-146">การดำเนินงานบริการที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a44b7-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="a44b7-147">เหตุผลอันดับแรกๆ ในการใช้การรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a44b7-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="a44b7-148">การรวมแบบสองทิศทางให้การรวมข้อมูลระหว่างแอพลิเคชัน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a44b7-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="a44b7-149">กรอบงานที่สมบูรณ์นี้เชื่อมโยงสภาพแวดล้อมและช่วยให้แอพลิเคชันธุรกิจต่างๆ สามารถทำงานร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="a44b7-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="a44b7-150">ต่อไปนี้เป็นเหตุผลอันดับแรกๆ ว่าทำไมคุณจึงควรใช้การรวมแบบสองทิศทาง:</span><span class="sxs-lookup"><span data-stu-id="a44b7-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="a44b7-151">การรวมแบบสองทิศทางให้การรวมแบบสองทิศทางที่ใกล้เรียลไทม์ซึ่งจับคู่กันระหว่างแอป Finance and Operations และแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a44b7-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="a44b7-152">การรวมนี้ทำให้ Microsoft Dynamics 365 เป็นร้านค้าครบวงจรสำหรับโซลูชันทางธุรกิจทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="a44b7-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="a44b7-153">ลูกค้าที่ใช้ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management แต่ผู้ที่ใช้โซลูชันที่ไม่ใช่ Microsoft สำหรับการจัดการความสัมพันธ์กับลูกค้า (CRM) กำลังย้ายไปยัง Dynamics 365 สำหรับการสนับสนุนการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a44b7-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="a44b7-154">ข้อมูลจากลูกค้า ผลิตภัณฑ์ การดำเนินงาน โครงการ และ Internet of Things (IoT) จะมีการหมุนเวียนโดยอัตโนมัติไปยัง Common Data Service ด้วยการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a44b7-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="a44b7-155">การเชื่อมต่อนี้มีประโยชน์มากสำหรับธุรกิจที่มีความสนใจในการขยาย Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="a44b7-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="a44b7-156">โครงสร้างพื้นฐานการรวมแบบสองทิศทางเป็นไปตามหลักการที่ไม่มีรหัส/รหัสต่ำ</span><span class="sxs-lookup"><span data-stu-id="a44b7-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="a44b7-157">ต้องใช้ความพยายามด้านวิศวกรรมที่น้อยที่สุดในการขยายแผนที่ตารางไปยังตาราง และเพื่อรวมแผนที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a44b7-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="a44b7-158">การรวมแบบสองทิศทางสนับสนุนทั้งโหมดออนไลน์และโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="a44b7-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="a44b7-159">Microsoft เป็นบริษัทเดียวที่มีการสนับสนุนสำหรับโหมดออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="a44b7-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="a44b7-160">การรวมแบบสองทิศทางหมายถึงอะไรสำหรับผู้ใช้และสถาปนิกของผลิตภัณฑ์ CRM</span><span class="sxs-lookup"><span data-stu-id="a44b7-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="a44b7-161">การรวมแบบสองทิศทางทำให้โฟลว์ข้อมูลระหว่างแอป Finance and Operations และ Common Data Service เป็นแบบอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a44b7-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="a44b7-162">ในรุ่นต่อๆ ไป แนวคิดในแอปที่เป็นแบบโมเดลใน Dynamics 365 (ตัวอย่างเช่น ลูกค้า ผู้ติดต่อ ใบเสนอราคา และใบสั่ง) จะได้รับการปรับให้เข้ากับลูกค้าในตลาดกลางและลูกค้าที่สูงกว่าตลาดกลาง</span><span class="sxs-lookup"><span data-stu-id="a44b7-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="a44b7-163">ในรุ่นแรก ส่วนใหญ่ของการทำงานอัตโนมัติถูกจัดการโดยโซลูชันการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a44b7-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="a44b7-164">ในรุ่นต่อๆ ไป โซลูชันเหล่านั้นจะกลายเป็นส่วนหนึ่งของ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="a44b7-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="a44b7-165">ด้วยการทำความเข้าใจถึงการเปลี่ยนแปลงที่กำลังจะเกิดขึ้นกับ Common Data Service คุณสามารถลดความพยายามของคุณได้ในระยะยาว</span><span class="sxs-lookup"><span data-stu-id="a44b7-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="a44b7-166">นี่คือบางส่วนของการเปลี่ยนแปลงที่สำคัญ:</span><span class="sxs-lookup"><span data-stu-id="a44b7-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="a44b7-167">Common Data Service จะมีแนวคิดใหม่ เช่น บริษัท และฝ่าย</span><span class="sxs-lookup"><span data-stu-id="a44b7-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="a44b7-168">แนวคิดเหล่านี้จะมีผลกระทบต่อแอปทั้งหมดที่สร้างขึ้นบน Common Data Service เช่น Dynamics 365 Sales Dynamics 365 Marketing Dynamics 365 Customer Service และ Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="a44b7-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="a44b7-169">กิจกรรมและบันทึกย่อถูกรวมและขยายเพื่อสนับสนุนทั้ง C1s (ผู้ใช้ของระบบ) และ C2s (ลูกค้าของระบบ)</span><span class="sxs-lookup"><span data-stu-id="a44b7-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="a44b7-170">นี่คือบางส่วนของการเปลี่ยนแปลงที่กำลังจะเกิดขึ้นใน Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="a44b7-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="a44b7-171">ชนิดข้อมูลทศนิยมจะแทนที่ชนิดข้อมูลของเงิน</span><span class="sxs-lookup"><span data-stu-id="a44b7-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="a44b7-172">วันที่มีผลบังคับใช้จะสนับสนุนข้อมูลในอดีต ในปัจจุบัน และในอนาคตในสถานที่เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a44b7-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="a44b7-173">จะมีการสนับสนุนเพิ่มเติมสำหรับสกุลเงินและอัตราแลกเปลี่ยน และจะมีการปรับปรุง Application Programming Interface (API) ของ **อัตราแลกเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="a44b7-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="a44b7-174">การแปลงหน่วยจะได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="a44b7-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="a44b7-175">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่กำลังจะเกิดขึ้น ดู [ข้อมูลใน Common Data Service – ระยะ 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap)</span><span class="sxs-lookup"><span data-stu-id="a44b7-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>
