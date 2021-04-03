---
title: ภาพรวมของการรวมแบบสองทิศทาง
description: หัวข้อนี้ให้การรวมแบบสองทิศทางภาพรวม ซึ่งให้การโต้ตอบแบบใกล้เรียลไทม์ระหว่างแอป Customer Engagement และแอป Finance and Operations
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6cc02b483a2975dd3be28032ea7e90b540945492
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561289"
---
# <a name="dual-write-overview"></a><span data-ttu-id="a23c0-103">ภาพรวมของการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a23c0-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="a23c0-104">การรวมแบบสองทิศทางคืออะไร</span><span class="sxs-lookup"><span data-stu-id="a23c0-104">What is dual-write?</span></span>

<span data-ttu-id="a23c0-105">การรวมแบบสองทิศทางเป็นโครงสร้างพื้นฐานแบบสำเร็จรูปที่ให้การโต้ตอบแบบใกล้เรียลไทม์ระหว่างแอป Customer Engagement และแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a23c0-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="a23c0-106">เมื่อข้อมูลเกี่ยวกับลูกค้า ผลิตภัณฑ์ บุคคล และการดำเนินงาน จะทำงานเกินขอบเขตของแอพลิเคชัน แผนกทั้งหมดในองค์กรมีอำนาจ</span><span class="sxs-lookup"><span data-stu-id="a23c0-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="a23c0-107">การรวมแบบสองทิศทางให้การรวมแบบสองทิศทางที่จับคู่กันระหว่างแอป Finance and Operations และ Dataverse</span><span class="sxs-lookup"><span data-stu-id="a23c0-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="a23c0-108">การเปลี่ยนแปลงข้อมูลใดๆ ในแอป Finance and Operations ทำให้เกิดการเขียนไปยัง Dataverse และการเปลี่ยนแปลงข้อมูลใดๆ ใน Dataverse ทำให้เกิดการเขียนไปยังแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a23c0-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="a23c0-109">โฟลว์ข้อมูลโดยอัตโนมัตินี้จะให้ประสบการณ์ผู้ใช้แบบรวมทั่วทั้งแอป</span><span class="sxs-lookup"><span data-stu-id="a23c0-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![ความสัมพันธ์ของข้อมูลระหว่างแอป](media/dual-write-overview.jpg)

<span data-ttu-id="a23c0-111">การรวมแบบสองทิศทางมีสองด้าน: ด้าน *โครงสร้างพื้นฐาน* และ *แอพลิเคชัน*</span><span class="sxs-lookup"><span data-stu-id="a23c0-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="a23c0-112">โครงสร้างพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="a23c0-112">Infrastructure</span></span>

<span data-ttu-id="a23c0-113">โครงสร้างพื้นฐานการรวมแบบสองทิศทางสามารถขยายได้และเชื่อถือได้ และรวมถึงคุณลักษณะที่สำคัญต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a23c0-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="a23c0-114">โฟลว์ข้อมูลแบบซิงโครนัสและแบบสองทิศทางระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="a23c0-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="a23c0-115">การซิงโครไนส์ร่วมกับโหมดเล่น หยุดชั่วคราว และติดตาม เพื่อสนับสนุนระบบในระหว่างโหมดอะซิงโครนัสแบบออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="a23c0-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="a23c0-116">ความสามารถในการซิงค์ข้อมูลเบื้องต้นระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="a23c0-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="a23c0-117">มุมมองรวมของกิจกรรมและล็อกข้อผิดพลาดสำหรับผู้ดูแลข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a23c0-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="a23c0-118">ความสามารถในการตั้งค่าคอนฟิกข้อความแจ้งเตือนและขีดจำกัดแบบกำหนดเอง และเพื่อบอกรับการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="a23c0-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="a23c0-119">อินเทอร์เฟสผู้ใช้ที่ใช้งานง่าย (UI) สำหรับการกรองข้อมูลและการแปลง</span><span class="sxs-lookup"><span data-stu-id="a23c0-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="a23c0-120">ความสามารถในการตั้งค่าและดูการขึ้นต่อกันและความสัมพันธ์ของตาราง</span><span class="sxs-lookup"><span data-stu-id="a23c0-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="a23c0-121">ความสามารถในการขยายสำหรับทั้งเอนทิตี้มาตรฐานและตารางแบบกำหนดเองและแผนผัง</span><span class="sxs-lookup"><span data-stu-id="a23c0-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="a23c0-122">การจัดการอายุการใช้งานแอพลิเคชันที่เชื่อถือได้</span><span class="sxs-lookup"><span data-stu-id="a23c0-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="a23c0-123">ประสบการณ์การตั้งค่าแบบสำเร็จรูปสำหรับลูกค้าใหม่</span><span class="sxs-lookup"><span data-stu-id="a23c0-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="a23c0-124">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="a23c0-124">Application</span></span>

<span data-ttu-id="a23c0-125">การรวมแบบสองทิศทางสร้างการแม็ประหว่างแนวคิดในแอป Finance and Operations และแนวคิดในแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a23c0-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="a23c0-126">การรวมนี้สนับสนุนสถานการณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a23c0-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="a23c0-127">ข้อมูลหลักของลูกค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a23c0-127">Integrated customer master</span></span>
+ <span data-ttu-id="a23c0-128">การเข้าถึงบัตรสมาชิกของลูกค้าและคะแนนรางวัล</span><span class="sxs-lookup"><span data-stu-id="a23c0-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="a23c0-129">ประสบการณ์ใช้งานผลิตภัณฑ์หลักแบบครบวงจร</span><span class="sxs-lookup"><span data-stu-id="a23c0-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="a23c0-130">การรับรู้ของลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="a23c0-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="a23c0-131">ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a23c0-131">Integrated vendor master</span></span>
+ <span data-ttu-id="a23c0-132">การเข้าถึงข้อมูลอ้างอิงทางการเงินและภาษี</span><span class="sxs-lookup"><span data-stu-id="a23c0-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="a23c0-133">ประสบการณ์ของกลไกจัดการราคาตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="a23c0-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="a23c0-134">ประสบการณ์ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสดแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a23c0-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="a23c0-135">ความสามารถในการให้บริการทั้งสินทรัพย์ภายในองค์กรและสินทรัพย์ของลูกค้าผ่านตัวแทนของฟิลด์</span><span class="sxs-lookup"><span data-stu-id="a23c0-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="a23c0-136">ประสบการณ์การสั่งซื้อจนถึงการได้รับเงินสดแบบรวม</span><span class="sxs-lookup"><span data-stu-id="a23c0-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="a23c0-137">กิจกรรมและบันทึกย่อแบบรวมสำหรับข้อมูลลูกค้าและเอกสาร</span><span class="sxs-lookup"><span data-stu-id="a23c0-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="a23c0-138">ความสามารถในการค้นหาความพร้อมของสินค้าคงคลังคงเหลือและรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="a23c0-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="a23c0-139">ความสามารถโครงการจนถึงการได้รับเงินสด</span><span class="sxs-lookup"><span data-stu-id="a23c0-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="a23c0-140">ความสามารถในการจัดการที่อยู่และบทบาทต่างๆ ผ่านแนวคิดของฝ่าย</span><span class="sxs-lookup"><span data-stu-id="a23c0-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="a23c0-141">การจัดการแหล่งข้อมูลเดียวสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="a23c0-141">Single source management for users</span></span>
+ <span data-ttu-id="a23c0-142">ช่องทางแบบรวมสำหรับการค้าปลีกและการตลาด</span><span class="sxs-lookup"><span data-stu-id="a23c0-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="a23c0-143">การมองเห็นในโปรโมชันและส่วนลด</span><span class="sxs-lookup"><span data-stu-id="a23c0-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="a23c0-144">ฟังก์ชันร้องขอการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="a23c0-144">Request-for-service functions</span></span>
+ <span data-ttu-id="a23c0-145">การดำเนินงานบริการที่มีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="a23c0-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="a23c0-146">เหตุผลอันดับแรกๆ ในการใช้การรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a23c0-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="a23c0-147">การรวมแบบสองทิศทางให้การรวมข้อมูลระหว่างแอพลิเคชัน Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a23c0-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="a23c0-148">กรอบงานที่สมบูรณ์นี้เชื่อมโยงสภาพแวดล้อมและช่วยให้แอพลิเคชันธุรกิจต่างๆ สามารถทำงานร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="a23c0-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="a23c0-149">ต่อไปนี้เป็นเหตุผลอันดับแรกๆ ว่าทำไมคุณจึงควรใช้การรวมแบบสองทิศทาง:</span><span class="sxs-lookup"><span data-stu-id="a23c0-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="a23c0-150">การรวมแบบสองทิศทางให้การรวมแบบสองทิศทางที่ใกล้เรียลไทม์ซึ่งจับคู่กันระหว่างแอป Finance and Operations และแอปที่เป็นแบบโมเดลใน Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a23c0-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="a23c0-151">การรวมนี้ทำให้ Microsoft Dynamics 365 เป็นร้านค้าครบวงจรสำหรับโซลูชันทางธุรกิจทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="a23c0-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="a23c0-152">ลูกค้าที่ใช้ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management แต่ผู้ที่ใช้โซลูชันที่ไม่ใช่ Microsoft สำหรับการจัดการความสัมพันธ์กับลูกค้า (CRM) กำลังย้ายไปยัง Dynamics 365 สำหรับการสนับสนุนการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a23c0-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="a23c0-153">ข้อมูลจากลูกค้า ผลิตภัณฑ์ การดำเนินงาน โครงการ และ Internet of Things (IoT) จะมีการหมุนเวียนโดยอัตโนมัติไปยัง Dataverse ด้วยการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="a23c0-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="a23c0-154">การเชื่อมต่อนี้มีประโยชน์สำหรับธุรกิจที่มีความสนใจในการขยาย Power Platform</span><span class="sxs-lookup"><span data-stu-id="a23c0-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="a23c0-155">โครงสร้างพื้นฐานการรวมแบบสองทิศทางเป็นไปตามหลักการที่ไม่มีรหัส/รหัสต่ำ</span><span class="sxs-lookup"><span data-stu-id="a23c0-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="a23c0-156">ต้องใช้ความพยายามด้านวิศวกรรมที่น้อยที่สุดในการขยายแผนที่ตารางไปยังตาราง และเพื่อรวมแผนที่ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="a23c0-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="a23c0-157">การรวมแบบสองทิศทางสนับสนุนทั้งโหมดออนไลน์และโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="a23c0-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="a23c0-158">Microsoft เป็นบริษัทเดียวที่มีการสนับสนุนสำหรับโหมดออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="a23c0-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="a23c0-159">การรวมแบบสองทิศทางหมายถึงอะไรสำหรับนักพัฒนาและสถาปนิกของแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a23c0-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="a23c0-160">การรวมแบบสองทิศทางทำให้โฟลว์ข้อมูลระหว่างแอป Finance and Operations และแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a23c0-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="a23c0-161">การรวมแบบสองทิศทางมีโซลูชัน AppSource สองรายการที่ติดตั้งบน Dataverse</span><span class="sxs-lookup"><span data-stu-id="a23c0-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="a23c0-162">โซลูชันนี้จะขยายเค้าร่างของตาราง ปลั๊กอิน และลำดับงานใน Dataverse เพื่อให้สามารถปรับขนาดของ ERP ได้</span><span class="sxs-lookup"><span data-stu-id="a23c0-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="a23c0-163">สำหรับการดำเนินงานที่ประสบความสำเร็จ นักพัฒนา และสถาปนิกของแอป Customer Engagement ต้องทำความเข้าใจการเปลี่ยนแปลงเหล่านี้และทำงานร่วมกันกับคู่ของพวกเขาบนแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a23c0-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="a23c0-164">เมื่อต้องการสร้างพาริตี้ที่มีแอปพลิเคชัน Finance and Operations การรวมแบบสองทิศทางทำให้เกิดการเปลี่ยนแปลงที่สำคัญบางอย่างในเค้าร่าง Dataverse</span><span class="sxs-lookup"><span data-stu-id="a23c0-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="a23c0-165">ถ้าคุณเข้าใจแผน คุณสามารถหลีกเลี่ยงการออกแบบและการพัฒนาบางอย่างใหม่ในอนาคตได้</span><span class="sxs-lookup"><span data-stu-id="a23c0-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="a23c0-166">เมื่อติดตั้งแพคเกจ AppSource การรวมแบบสองทิศทาง Dataverse จะมีแนวคิดใหม่ เช่น บริษัทและฝ่าย</span><span class="sxs-lookup"><span data-stu-id="a23c0-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="a23c0-167">แนวคิดเหล่านี้จะช่วยให้แอปพลิเคชันที่สร้างใน Dataverse รวมถึง Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service และ Dynamics 365 Field Service สามารถโต้ตอบกับแอป Finance and Operations ได้อย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="a23c0-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="a23c0-168">กิจกรรมและบันทึกย่อถูกรวมและขยายเพื่อสนับสนุนทั้ง C1s (ผู้ใช้ของระบบ) และ C2s (ลูกค้าของระบบ)</span><span class="sxs-lookup"><span data-stu-id="a23c0-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="a23c0-169">หากต้องการป้องกันไม่ให้ข้อมูลสูญหายระหว่างการส่งผ่านสกุลเงินระหว่างแอป Finance and Operations และ Dataverse คุณจะสามารถขยายจำนวนตำแหน่งทศนิยมในชนิดข้อมูลสกุลเงินของแอป Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="a23c0-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="a23c0-170">คุณลักษณะนี้จะแปลแถวที่มีอยู่โดยอัตโนมัติไปเป็นสถานะแบบขยายใหม่ที่เลเยอร์ข้อมูลเมตา</span><span class="sxs-lookup"><span data-stu-id="a23c0-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="a23c0-171">ในระหว่างกระบวนการนี้ จะมีการแปลค่าสกุลเงินเป็นข้อมูลทศนิยมแทนข้อมูลเงิน และค่าสกุลเงินที่รองรับทศนิยม10 ตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="a23c0-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="a23c0-172">คุณลักษณะนี้จะมีการเลือกใช้ และองค์กรที่ไม่จำเป็นต้องมีทศนิยมมากกว่า 4 ตำแหน่งของความแม่นยำไม่จำเป็นต้องเลือกใช้</span><span class="sxs-lookup"><span data-stu-id="a23c0-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="a23c0-173">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การย้ายชนิดข้อมูลสกุลเงินสำหรับการรวมแบบสองทิศทาง](currrency-decimal-places.md)</span><span class="sxs-lookup"><span data-stu-id="a23c0-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="a23c0-174">[วันที่มีผลบังคับใช้](../../dev-tools/date-effectivity.md) จะมีการเพิ่มลงใน Dataverse</span><span class="sxs-lookup"><span data-stu-id="a23c0-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="a23c0-175">ซึ่งจะสนับสนุนข้อมูลในอดีต ในปัจจุบัน และในอนาคต ในตารางเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="a23c0-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="a23c0-176">[การแปลงหน่วย](../../../../supply-chain/pim/tasks/manage-unit-measure.md) ผลิตภัณฑ์ได้รับการสนับสนุนสำหรับผลิตภัณฑ์ ใบเสนอราคา ใบสั่ง และใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a23c0-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="a23c0-177">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่กำลังจะเกิดขึ้น โปรดดู [มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างในการรวมแบบสองทิศทาง](whats-new-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="a23c0-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]