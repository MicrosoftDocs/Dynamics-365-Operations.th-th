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
ms.openlocfilehash: 1eb5e4ea8d086baeee686ccb3d044b3ef9d2a4fa
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818583"
---
# <a name="dual-write-overview"></a><span data-ttu-id="63648-104">ภาพรวมของการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63648-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="63648-105">การรวมแบบสองทิศทางคืออะไร</span><span class="sxs-lookup"><span data-stu-id="63648-105">What is dual-write?</span></span>

<span data-ttu-id="63648-106">การรวมแบบสองทิศทางเป็นโครงสร้างพื้นฐานแบบสำเร็จรูปที่ให้การโต้ตอบแบบใกล้เรียลไทม์ระหว่างแอป Customer Engagement และแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63648-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="63648-107">เมื่อข้อมูลเกี่ยวกับลูกค้า ผลิตภัณฑ์ บุคคล และการดำเนินงาน จะทำงานเกินขอบเขตของแอพลิเคชัน แผนกทั้งหมดในองค์กรมีอำนาจ</span><span class="sxs-lookup"><span data-stu-id="63648-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="63648-108">การรวมแบบสองทิศทางให้การรวมแบบสองทิศทางที่จับคู่กันระหว่างแอป Finance and Operations และ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="63648-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="63648-109">การเปลี่ยนแปลงข้อมูลใดๆ ในแอป Finance and Operations ทำให้เกิดการเขียนไปยัง Common Data Service และการเปลี่ยนแปลงข้อมูลใดๆ ใน Common Data Service ทำให้เกิดการเขียนไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63648-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="63648-110">โฟลว์ข้อมูลโดยอัตโนมัตินี้จะให้ประสบการณ์ผู้ใช้แบบรวมทั่วทั้งแอป</span><span class="sxs-lookup"><span data-stu-id="63648-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![ความสัมพันธ์ของข้อมูลระหว่างแอป](media/dual-write-overview.jpg)

<span data-ttu-id="63648-112">การรวมแบบสองทิศทางมีสองด้าน: ด้าน *โครงสร้างพื้นฐาน* และ *แอพลิเคชัน*</span><span class="sxs-lookup"><span data-stu-id="63648-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="63648-113">โครงสร้างพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="63648-113">Infrastructure</span></span>

<span data-ttu-id="63648-114">โครงสร้างพื้นฐานการรวมแบบสองทิศทางสามารถขยายได้และเชื่อถือได้ และรวมถึงคุณลักษณะที่สำคัญต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="63648-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="63648-115">โฟลว์ข้อมูลแบบซิงโครนัสและแบบสองทิศทางระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="63648-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="63648-116">การซิงโครไนส์ร่วมกับโหมดเล่น หยุดชั่วคราว และติดตาม เพื่อสนับสนุนระบบในระหว่างโหมดอะซิงโครนัสแบบออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="63648-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="63648-117">ความสามารถในการซิงค์ข้อมูลเบื้องต้นระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="63648-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="63648-118">มุมมองรวมของกิจกรรมและล็อกข้อผิดพลาดสำหรับผู้ดูแลข้อมูล</span><span class="sxs-lookup"><span data-stu-id="63648-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="63648-119">ความสามารถในการตั้งค่าคอนฟิกข้อความแจ้งเตือนและขีดจำกัดแบบกำหนดเอง และเพื่อบอกรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="63648-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="63648-120">อินเทอร์เฟสผู้ใช้ที่ใช้งานง่าย (UI) สำหรับการกรองข้อมูลและการแปลง</span><span class="sxs-lookup"><span data-stu-id="63648-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="63648-121">ความสามารถในการตั้งค่าและดูการที่ขึ้นต่อกันกับเอนทิตี้และความสัมพันธ์</span><span class="sxs-lookup"><span data-stu-id="63648-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="63648-122">ความสามารถในการขยายสำหรับทั้งเอนทิตี้มาตรฐานและเอนทิตี้แบบกำหนดเองและแผนผัง</span><span class="sxs-lookup"><span data-stu-id="63648-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="63648-123">การจัดการอายุการใช้งานแอพลิเคชันที่เชื่อถือได้</span><span class="sxs-lookup"><span data-stu-id="63648-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="63648-124">ประสบการณ์การตั้งค่าแบบสำเร็จรูปสำหรับลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="63648-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="63648-125">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="63648-125">Application</span></span>

<span data-ttu-id="63648-126">การรวมแบบสองทิศทางสร้างการแม็ประหว่างแนวคิดในแอป Finance and Operations และแนวคิดในแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="63648-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="63648-127">การรวมนี้สนับสนุนสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="63648-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="63648-128">ข้อมูลหลักของลูกค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="63648-128">Integrated customer master</span></span>
+ <span data-ttu-id="63648-129">การเข้าถึงบัตรสมาชิกของลูกค้าและคะแนนรางวัล</span><span class="sxs-lookup"><span data-stu-id="63648-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="63648-130">ประสบการณ์ใช้งานผลิตภัณฑ์หลักแบบครบวงจร</span><span class="sxs-lookup"><span data-stu-id="63648-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="63648-131">การรับรู้ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="63648-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="63648-132">ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม</span><span class="sxs-lookup"><span data-stu-id="63648-132">Integrated vendor master</span></span>
+ <span data-ttu-id="63648-133">การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="63648-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="63648-134">ประสบการณ์ของกลไกจัดการราคาตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="63648-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="63648-135">ประสบการณ์ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดแบบรวม</span><span class="sxs-lookup"><span data-stu-id="63648-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="63648-136">ความสามารถในการให้บริการทั้งสินทรัพย์ภายในองค์กรและสินทรัพย์ของลูกค้าผ่านตัวแทนของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="63648-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="63648-137">ประสบการณ์การสั่งซื้อจนถึงการได้รับเงินสดแบบรวม</span><span class="sxs-lookup"><span data-stu-id="63648-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="63648-138">กิจกรรมและบันทึกย่อแบบรวมสำหรับข้อมูลลูกค้าและเอกสาร</span><span class="sxs-lookup"><span data-stu-id="63648-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="63648-139">ความสามารถในการค้นหาความพร้อมของสินค้าคงคลังคงเหลือและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="63648-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="63648-140">ความสามารถโครงการจนถึงการได้รับเงินสด</span><span class="sxs-lookup"><span data-stu-id="63648-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="63648-141">ความสามารถในการจัดการที่อยู่และบทบาทต่างๆ ผ่านแนวคิดของฝ่าย</span><span class="sxs-lookup"><span data-stu-id="63648-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="63648-142">การจัดการแหล่งข้อมูลเดียวสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="63648-142">Single source management for users</span></span>
+ <span data-ttu-id="63648-143">ช่องทางแบบรวมสำหรับการค้าปลีกและการตลาด</span><span class="sxs-lookup"><span data-stu-id="63648-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="63648-144">การมองเห็นในโปรโมชันและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="63648-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="63648-145">ฟังก์ชันร้องขอการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="63648-145">Request-for-service functions</span></span>
+ <span data-ttu-id="63648-146">การดำเนินงานบริการที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="63648-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="63648-147">เหตุผลอันดับแรกๆ ในการใช้การรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63648-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="63648-148">การรวมแบบสองทิศทางให้การรวมข้อมูลระหว่างแอพลิเคชัน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="63648-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="63648-149">กรอบงานที่สมบูรณ์นี้เชื่อมโยงสภาพแวดล้อมและช่วยให้แอพลิเคชันธุรกิจต่างๆ สามารถทำงานร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="63648-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="63648-150">ต่อไปนี้เป็นเหตุผลอันดับแรกๆ ว่าทำไมคุณจึงควรใช้การรวมแบบสองทิศทาง:</span><span class="sxs-lookup"><span data-stu-id="63648-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="63648-151">การรวมแบบสองทิศทางให้การรวมแบบสองทิศทางที่ใกล้เรียลไทม์ซึ่งจับคู่กันระหว่างแอป Finance and Operations และแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="63648-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="63648-152">การรวมนี้ทำให้ Microsoft Dynamics 365 เป็นร้านค้าครบวงจรสำหรับโซลูชันทางธุรกิจทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="63648-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="63648-153">ลูกค้าที่ใช้ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management แต่ผู้ที่ใช้โซลูชันที่ไม่ใช่ Microsoft สำหรับการจัดการความสัมพันธ์กับลูกค้า (CRM) กำลังย้ายไปยัง Dynamics 365 สำหรับการสนับสนุนการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63648-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="63648-154">ข้อมูลจากลูกค้า ผลิตภัณฑ์ การดำเนินงาน โครงการ และ Internet of Things (IoT) จะมีการหมุนเวียนโดยอัตโนมัติไปยัง Common Data Service ด้วยการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="63648-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="63648-155">การเชื่อมต่อนี้มีประโยชน์สำหรับธุรกิจที่มีความสนใจในการขยาย Power Platform</span><span class="sxs-lookup"><span data-stu-id="63648-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="63648-156">โครงสร้างพื้นฐานการรวมแบบสองทิศทางเป็นไปตามหลักการที่ไม่มีรหัส/รหัสต่ำ</span><span class="sxs-lookup"><span data-stu-id="63648-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="63648-157">ต้องใช้ความพยายามด้านวิศวกรรมที่น้อยที่สุดในการขยายแผนที่ตารางไปยังตาราง และเพื่อรวมแผนที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="63648-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="63648-158">การรวมแบบสองทิศทางสนับสนุนทั้งโหมดออนไลน์และโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="63648-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="63648-159">Microsoft เป็นบริษัทเดียวที่มีการสนับสนุนสำหรับโหมดออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="63648-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="63648-160">การรวมแบบสองทิศทางหมายถึงอะไรสำหรับนักพัฒนาและสถาปนิกของแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="63648-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="63648-161">การรวมแบบสองทิศทางทำให้โฟลว์ข้อมูลระหว่างแอป Finance and Operations และแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="63648-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="63648-162">การรวมแบบสองทิศทางมีโซลูชัน AppSource สองรายการที่ติดตั้งบน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="63648-162">Dual-write consists of two AppSource solutions that are installed on Common Data Service.</span></span> <span data-ttu-id="63648-163">โซลูชันนี้จะขยายเค้าร่างของเอนทิตี้ ปลั๊กอิน และลำดับงานใน Common Data Service เพื่อให้สามารถปรับขนาดของ ERP ได้</span><span class="sxs-lookup"><span data-stu-id="63648-163">The solutions expand the entity schema, plugins, and workflows on Common Data Service so that they can scale to ERP size.</span></span> <span data-ttu-id="63648-164">สำหรับการดำเนินงานที่ประสบความสำเร็จ นักพัฒนา และสถาปนิกของแอป Customer Engagement ต้องทำความเข้าใจการเปลี่ยนแปลงเหล่านี้และทำงานร่วมกันกับคู่ของพวกเขาบนแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63648-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="63648-165">เมื่อต้องการสร้างพาริตี้ที่มีแอปพลิเคชัน Finance and Operations การรวมแบบสองทิศทางทำให้เกิดการเปลี่ยนแปลงที่สำคัญบางอย่างในเค้าร่าง Common Data Service</span><span class="sxs-lookup"><span data-stu-id="63648-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Common Data Service schema.</span></span> <span data-ttu-id="63648-166">ถ้าคุณเข้าใจแผน คุณสามารถหลีกเลี่ยงการออกแบบและการพัฒนาบางอย่างใหม่ในอนาคตได้</span><span class="sxs-lookup"><span data-stu-id="63648-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="63648-167">เมื่อติดตั้งแพคเกจ AppSource การรวมแบบสองทิศทาง Common Data Service จะมีแนวคิดใหม่ เช่น บริษัทและฝ่าย</span><span class="sxs-lookup"><span data-stu-id="63648-167">When the dual-write AppSource package is installed, Common Data Service will have new concepts such as company and party.</span></span> <span data-ttu-id="63648-168">แนวคิดเหล่านี้จะช่วยให้แอปพลิเคชันที่สร้างใน Common Data Service รวมถึง Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service และ Dynamics 365 Field Service สามารถโต้ตอบกับแอป Finance and Operations ได้อย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="63648-168">These concepts help applications built on Common Data Service, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="63648-169">กิจกรรมและบันทึกย่อถูกรวมและขยายเพื่อสนับสนุนทั้ง C1s (ผู้ใช้ของระบบ) และ C2s (ลูกค้าของระบบ)</span><span class="sxs-lookup"><span data-stu-id="63648-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="63648-170">หากต้องการป้องกันไม่ให้ข้อมูลสูญหายระหว่างการส่งผ่านสกุลเงินระหว่างแอป Finance and Operations และ Common Data Service คุณจะสามารถขยายจำนวนตำแหน่งทศนิยมในชนิดข้อมูลสกุลเงินของแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="63648-170">To prevent data loss during currency transmission between Finance and Operations apps and the Common Data Service, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="63648-171">คุณลักษณะนี้จะแปลเรกคอร์ดที่มีอยู่โดยอัตโนมัติไปเป็นสถานะแบบขยายใหม่ที่เลเยอร์ข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="63648-171">The feature autotranslates existing records to the new extended state at the metadata layer.</span></span> <span data-ttu-id="63648-172">ในระหว่างกระบวนการนี้ จะมีการแปลค่าสกุลเงินเป็นข้อมูลทศนิยมแทนข้อมูลเงิน และค่าสกุลเงินที่รองรับทศนิยม10 ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="63648-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="63648-173">คุณลักษณะนี้จะมีการเลือกใช้ และองค์กรที่ไม่จำเป็นต้องมีทศนิยมมากกว่า 4 ตำแหน่งของความแม่นยำไม่จำเป็นต้องเลือกใช้</span><span class="sxs-lookup"><span data-stu-id="63648-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="63648-174">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การย้ายชนิดข้อมูลสกุลเงินสำหรับการรวมแบบสองทิศทาง](currrency-decimal-places.md)</span><span class="sxs-lookup"><span data-stu-id="63648-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="63648-175">[วันที่มีผลบังคับใช้](../../dev-tools/date-effectivity.md) จะมีการเพิ่มลงใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="63648-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Common Data Service.</span></span> <span data-ttu-id="63648-176">ซึ่งจะสนับสนุนข้อมูลในอดีต ในปัจจุบัน และในอนาคตในเอนทิตี้เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="63648-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="63648-177">[การแปลงหน่วย](../../../../supply-chain/pim/tasks/manage-unit-measure.md) ผลิตภัณฑ์ได้รับการสนับสนุนสำหรับผลิตภัณฑ์ ใบเสนอราคา ใบสั่ง และใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="63648-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="63648-178">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่กำลังจะเกิดขึ้น โปรดดู [มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างในการรวมแบบสองทิศทาง](whats-new-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="63648-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

