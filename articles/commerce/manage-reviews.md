---
title: จัดการการให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายถึงวิธีการจัดการการจัดอันดับและแสดงความคิดเห็นในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 60ad0dd821dc91576a59cf73ec46da4aefd34a2f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794270"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="efdc8-103">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="efdc8-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="efdc8-104">หัวข้อนี้จะอธิบายถึงวิธีการจัดการการจัดอันดับและแสดงความคิดเห็นในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="efdc8-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="efdc8-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="efdc8-105">Overview</span></span>

<span data-ttu-id="efdc8-106">Dynamics 365 Commerce ใช้บริการองค์ความรู้ Microsoft Azure เพื่อตรวจสอบข้อความความคิดเห็นโดยอัตโนมัติโดยการแก้ไขคำหยาบ</span><span class="sxs-lookup"><span data-stu-id="efdc8-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="efdc8-107">นอกจากนี้ ผู้ดูแลสามารถใช้โปรแกรมสร้างไซต์ Dynamics 365 Commerce เพื่อใช้ทำงานที่กำหนดด้วยตนเองดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="efdc8-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="efdc8-108">ตรวจทานความคิดเห็นโดยตอบกลับหรือลบออก</span><span class="sxs-lookup"><span data-stu-id="efdc8-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="efdc8-109">ลบความคิดเห็นของลูกค้าตามคำขอของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="efdc8-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="efdc8-110">การนำเข้าการจัดอันดับและข้อมูลความคิดเห็นจำนวนมากของผลิตภัณฑ์ทั้งหมดที่นำเข้าในเท็มเพลต Microsoft Power BI เพื่อให้สามารถวิเคราะห์แนวโน้มของการจัดอันดับและการความคิดเห็นได้</span><span class="sxs-lookup"><span data-stu-id="efdc8-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="efdc8-111">อ่านความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-111">Read a review</span></span> 

<span data-ttu-id="efdc8-112">หากต้องการอ่านความคิดเห็นในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-113">ไปที่ **หน้าแรก\> ความคิดเห็น \> การตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="efdc8-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="efdc8-114">ใช้ฟิลด์ค้นหาที่ด้านขวาบนของหน้าเพื่อกรองความคิดเห็นที่แสดงตามรหัสผลิตภัณฑ์ ชื่อผลิตภัณฑ์ หรือข้อความความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="efdc8-115">ตัวกรองข้อมูลเพิ่มเติมจะช่วยให้คุณสามารถจำกัดความคิดเห็นโดยเรียงตามรอบระยะเวลา การจัดอันดับ ช่องทาง หรือสถานะของปัญหา (นำลง ตอบสนอง หรือรายงาน)</span><span class="sxs-lookup"><span data-stu-id="efdc8-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![การตรวจสอบโฮมเพจ](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="efdc8-117">ตอบสนองความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-117">Respond to a review</span></span> 

<span data-ttu-id="efdc8-118">บางครั้งลูกค้าที่ซื้อผลิตภัณฑ์แสดงความพึงพอใจหรือความไม่พอใจของตนเอง หรือไม่เข้าใจวิธีการใช้ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="efdc8-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="efdc8-119">ในฐานะผู้ดูแลคุณสามารถลงรายการบัญชีการตอบสนองความคิดเห็นได้</span><span class="sxs-lookup"><span data-stu-id="efdc8-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="efdc8-120">การตอบสนองนี้จะปรากฏพร้อมกับความคิดเห็นบนไซต์</span><span class="sxs-lookup"><span data-stu-id="efdc8-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="efdc8-121">หากต้องการตอบสนองต่อความคิดเห็นในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-122">ไปที่ **หน้าแรก\> ความคิดเห็น \> การตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="efdc8-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="efdc8-123">ค้นหาและเลือกความคิดเห็นที่จำเป็นต้องมีการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="efdc8-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="efdc8-124">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือก **เพิ่มการตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="efdc8-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="efdc8-125">ป้อนข้อความตอบสนองและชื่อที่ควรแสดงสำหรับผู้ตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="efdc8-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="efdc8-126">ชื่อผู้ตอบสนองเริ่มต้นคือ **ผู้ดูแล**</span><span class="sxs-lookup"><span data-stu-id="efdc8-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="efdc8-127">เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **โพสต์การตอบสนอง**</span><span class="sxs-lookup"><span data-stu-id="efdc8-127">When you've finished, select **Post response**.</span></span>

![กำลังตอบสนองต่อการตรวจทาน](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="efdc8-129">นำความคิดเห็นออก</span><span class="sxs-lookup"><span data-stu-id="efdc8-129">Take down a review</span></span> 

<span data-ttu-id="efdc8-130">บางครั้งมีเหตุผลทางธุรกิจสำหรับผู้ควบคุมที่จะนำความคิดเห็นของลูกค้าออก</span><span class="sxs-lookup"><span data-stu-id="efdc8-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="efdc8-131">หากต้องการนำความคิดเห็นในโปรแกรมสร้างไซต์ Commerce ออก ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-132">ไปที่ **หน้าแรก\> ความคิดเห็น \> การตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="efdc8-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="efdc8-133">ค้นหาและเลือกความคิดเห็นที่ต้องนำออก</span><span class="sxs-lookup"><span data-stu-id="efdc8-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="efdc8-134">ในบานหน้าต่างคุณสมบัติทางด้านขวา ให้เลือกเหตุผลของการนำออกภายใต้  **ความคิดเห็น Takedown** จากนั้นเลือก **นำออก**</span><span class="sxs-lookup"><span data-stu-id="efdc8-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="efdc8-135">ลบความคิดเห็นของลูกค้าตามคำขอของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="efdc8-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="efdc8-136">บางครั้งลูกค้าต้องการให้การจัดอันดับและข้อมูลความคิดเห็นของพวกเขาถูกลบออกจากเว็บไซต์อีคอมเมิร์ซอย่างถาวร</span><span class="sxs-lookup"><span data-stu-id="efdc8-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="efdc8-137">ผู้ควบคุมที่รับคำขอให้ลบออกจากลูกค้าอาจลบข้อมูลของลูกค้าโดยใช้ลักษณะการทำงานการลบความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="efdc8-138">ในการค้นหาและลบข้อมูลของลูกค้า ผู้ดูแลต้องมีที่อยู่อีเมลที่ลูกค้าใช้ในการลงชื่อเข้าใช้และให้ความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="efdc8-139">เมื่อต้องการค้นหาและลบข้อมูลลูกค้าในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-140">ไปที่ **หน้าแรก \> ความคิดเห็น \> ลบ**</span><span class="sxs-lookup"><span data-stu-id="efdc8-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="efdc8-141">ในกล่อง **ค้นหาผู้ใช้ตามที่อยู่อีเมล** ให้ป้อนที่อยู่อีเมลของลูกค้าแล้วเลือก **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="efdc8-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="efdc8-142">ถ้าลูกค้ามีกิจกรรมความคิดเห็นใดๆ (ตัวอย่างเช่น การส่งความคิดเห็น การโหวตเกี่ยวกับการให้ความช่วยเหลือของความคิดเห็นลูกค้าคนอื่น) หรือแสดงความคิดเห็นบนความคิดเห็นของลูกค้าคนอื่น ผลลัพธ์จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="efdc8-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="efdc8-143">สำหรับสินค้าแต่ละรายการจะมีปุ่ม **ลบ**</span><span class="sxs-lookup"><span data-stu-id="efdc8-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="efdc8-144">สำหรับสินค้าแต่ละรายการที่ต้องลบ ให้เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="efdc8-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="efdc8-145">เมื่อคุณได้รับข้อความแจ้งยืนยัน ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="efdc8-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![การลบข้อมูลของลูกค้า](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="efdc8-147">การทำเช่นนี้อาจใช้เวลาเจ็ดวันสำหรับการลบข้อมูลออกจากระบบโดยสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="efdc8-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="efdc8-148">ผู้ดูแลควรแจ้งให้ลูกค้าทราบเกี่ยวกับความล่าช้านี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="efdc8-149">ถ้าลูกค้ามีการเปลี่ยนแปลงชื่อในการตั้งค่าบัญชีของผู้ใช้ แต่ละรายการอาจปรากฏขึ้นในผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="efdc8-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="efdc8-150">ในกรณีนี้เมื่อต้องการลบข้อมูลของลูกค้าอย่างสมบูรณ์ ผู้ดูแลต้องเลือก **ลบ** สำหรับสินค้าแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="efdc8-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="efdc8-151">ดาวน์โหลดข้อมูลการจัดอันดับและความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-151">Download ratings and reviews data</span></span>

<span data-ttu-id="efdc8-152">โปรแกรมสร้างไซต์ Commerce ช่วยให้ผู้ดูแลนำเข้าข้อมูลการจัดอันดับและความคิดเห็นจำนวนมากเพื่อให้สามารถวิเคราะห์แนวโน้มได้</span><span class="sxs-lookup"><span data-stu-id="efdc8-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="efdc8-153">เท็มเพลต Power BI ที่มีการวัดพื้นฐานจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="efdc8-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="efdc8-154">ผู้ควบคุมสามารถใช้เท็มเพลตนี้เพื่อเชื่อมต่อกับข้อมูลที่นำเข้าจำนวนมากและดูแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="efdc8-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="efdc8-155">ผู้ใช้เหล่านั้นไม่จำเป็นต้องสร้างแดชบอร์ดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="efdc8-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="efdc8-156">ผู้ดูแลยังสามารถเลือกกำหนดเท็มเพลต Power BI เองเพื่อตอบสนองความต้องการเฉพาะของตนเองได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="efdc8-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="efdc8-157">เมื่อต้องการดาวน์โหลดข้อมูลการจัดอันดับและความคิดเห็นในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-158">ไปที่ **หน้าแรก \> ความคิดเห็น \> การรายงาน**</span><span class="sxs-lookup"><span data-stu-id="efdc8-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="efdc8-159">เลือก **ดาวน์โหลดข้อมูลคามคิดเห็น** เพื่อดาวน์โหลดข้อมูลการจัดอันดับและความคิดเห็นจำนวนมากในรูปแบบมูลค่าที่คั่นด้วยเครื่องหมายจุลภาค (CSV)</span><span class="sxs-lookup"><span data-stu-id="efdc8-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="efdc8-160">ดูแนวโน้มการให้คะแนนและความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-160">View ratings and reviews trends</span></span>

<span data-ttu-id="efdc8-161">ผู้ดูแลสามารถดาวน์โหลดเท็มเพลต Power BI เพื่อให้สามารถดูแนวโน้มในแดชบอร์ดได้</span><span class="sxs-lookup"><span data-stu-id="efdc8-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="efdc8-162">เมื่อต้องการดูแนวโน้มการจัดอันดับและความคิดเห็นในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="efdc8-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-163">ไปที่ **หน้าแรก \> ความคิดเห็น \> การรายงาน**</span><span class="sxs-lookup"><span data-stu-id="efdc8-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="efdc8-164">เลือก **เท็มเพลต PowerBI** เพื่อดาวน์โหลดเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="efdc8-164">Select **PowerBI template** to download the template.</span></span>

    ![ดาวน์โหลดแม่แบบ Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="efdc8-166">เปิดเท็มเพลตที่ดาวน์โหลดโดยใช้แอป Power BI</span><span class="sxs-lookup"><span data-stu-id="efdc8-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="efdc8-167">ปิดกล่องโต้ตอบ **การเข้าถึงเนื้อหาเว็บ** ที่ปรากฏ แล้วปิดข้อความแสดงข้อผิดพลาด "รีเฟรช" ที่ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="efdc8-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="efdc8-168">ไปที่ **หน้าแรก** เลือก **แก้ไขการสอบถาม** แล้วเลือก **การตั้งค่าแหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="efdc8-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="efdc8-169">ในกล่อง **การตั้งค่าแหล่งข้อมูล** ให้เลือก **แหล่งที่มา**</span><span class="sxs-lookup"><span data-stu-id="efdc8-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="efdc8-170">ในฟิลด์ **URL** ให้ป้อนพาธของข้อมูลความคิดเห็นที่คุณดาวน์โหลดไว้ในขั้นตอนก่อนหน้านี้ (ตัวอย่างเช่น **c:\\reviews\\ReviewsData.csv**)</span><span class="sxs-lookup"><span data-stu-id="efdc8-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![ฟิลด์ URL ในกล่องโต้ตอบค่าที่แบ่งด้วยเครื่องหมายจุลภาค](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="efdc8-172">เลือก **ตกลง** แล้วเลือก **ปรับใช้การเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="efdc8-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="efdc8-173">การดำเนินการนี้จะใช้เวลาหนึ่งถึงสองนาทีในการใช้การเปลี่ยนแปลงของคุณกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="efdc8-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="efdc8-174">เลือก **แผ่นแนวโน้ม** เพื่อดูการให้คะแนนและแนวโน้มความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="efdc8-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![แนวโน้มการให้คะแนนและความคิดเห็น](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="efdc8-176">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="efdc8-176">Additional resources</span></span>

[<span data-ttu-id="efdc8-177">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="efdc8-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="efdc8-178">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="efdc8-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="efdc8-179">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="efdc8-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="efdc8-180">ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="efdc8-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]