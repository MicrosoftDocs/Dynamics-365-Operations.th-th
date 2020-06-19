---
title: ยกเลิกคำแนะนำส่วนบุคคล
description: หัวข้อนี้อธิบายวิธีที่คุณสามารถให้ลูกค้าเลือกที่จะไม่รับคำแนะนำแบบส่วนตัวใน Microsoft Dynamics 365 Commerce
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87c031c045249dbcde274d7c741beb72c3216aa8
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404290"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="45138-103">ยกเลิกคำแนะนำส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="45138-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="45138-104">หัวข้อนี้อธิบายวิธีที่คุณสามารถให้ลูกค้าเลือกที่จะไม่รับคำแนะนำแบบส่วนตัวใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="45138-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="45138-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="45138-105">Overview</span></span>

<span data-ttu-id="45138-106">ในระหว่างการสร้างลูกค้าองค์กร ลูกค้าใหม่จะได้รับการตั้งค่าโดยอัตโนมัติเพื่อรับคำแนะนำแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="45138-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="45138-107">อย่างไรก็ตาม Dynamics 365 Commerce มีวิธีการต่างๆสำหรับผู้ค้าปลีกเพื่อให้ผู้ใช้เลือกที่จะไม่รับคำแนะนำเหล่านี้ และจำกัด การประมวลผลข้อมูลส่วนบุคคลของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="45138-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="45138-108">ผู้ใช้ที่ได้รับการรับรองความถูกต้องซึ่งไม่เข้าร่วมรับคำแนะนำแบบส่วนตัวจะหยุดการดูรายการแบบส่วนตัวในทันที</span><span class="sxs-lookup"><span data-stu-id="45138-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="45138-109">นอกจากนี้ ข้อมูลส่วนบุคคลทั้งหมดที่เก็บรวบรวมสำหรับการตั้งค่าส่วนบุคคลจะถูกลบออกจากโมเดลคำแนะนำแบบส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="45138-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="45138-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำแนะนำผลิตภัณฑ์แบบส่วนตัว โปรดดู [เปิดใช้งานคำแนะนำแบบส่วนตัว](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="45138-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="45138-111">วิธีที่ผู้ค้าปลีกจะใช้ประสบการณ์การปฏิเสธเข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="45138-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="45138-112">ผู้ค้าปลีกมีสามวิธีที่จะใช้ประสบการณ์การปฏิเสธเข้าร่วม</span><span class="sxs-lookup"><span data-stu-id="45138-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="45138-113">ปฏิเสธเข้าร่วมที่กระทำในนามของผู้ใช้อื่น</span><span class="sxs-lookup"><span data-stu-id="45138-113">Opting out on behalf of users</span></span>

<span data-ttu-id="45138-114">ในการจัดการลูกค้าองค์กรในการสนับสนุนการค้า ผู้ค้าปลีกสามารถปฏิเสธเข้าร่วมในนามของผู้ใช้อื่น</span><span class="sxs-lookup"><span data-stu-id="45138-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="45138-115">จากหน้าแรกของการสนับสนุน ให้ค้นหา **ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="45138-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="45138-116">ค้นหาและเลือกลูกค้า จากนั้นเลือก FastTab **การขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="45138-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![FastTab การขายปลีก](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="45138-118">ภายใต้ **ความเป็นส่วนตัว** ตั้งค่าตัวเลือก **ปิดใช้งานการตั้งค่าส่วนบุคคล** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="45138-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![การตั้งค่าความเป็นส่วนตัว](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="45138-120">เลือก **บันทึก** และปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="45138-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="45138-121">ประสบการณ์การเลือกไม่ใช้การยึดตามโมดูล</span><span class="sxs-lookup"><span data-stu-id="45138-121">Module-based opt-out experience</span></span>

<span data-ttu-id="45138-122">ผู้ค้าปลีกสามารถอนุญาตให้ผู้ใช้ที่ผ่านการรับรองความถูกต้องยกเลิกคำแนะนำแบบส่วนตัวได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="45138-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="45138-123">เพื่อมอบประสบการณ์การไม่เข้าร่วมนี้ ให้เพิ่มโมดูลการยกเลิกผู้ใช้ในหน้าโปรไฟล์บัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="45138-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="45138-124">ส่วนขยายที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="45138-124">Custom extensions</span></span>

<span data-ttu-id="45138-125">ผู้ค้าปลีกสามารถสร้างส่วนขยายของตนเองเพื่อจัดการประสบการณ์การเลือกไม่ใช้สำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="45138-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="45138-126">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [เรียกเซิร์ฟเวอร์การขายปลีก API](e-commerce-extensibility/call-retail-server-apis.md) และ [การเพิ่มช่องทางออนไลน์](e-commerce-extensibility/overview.md)</span><span class="sxs-lookup"><span data-stu-id="45138-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="45138-127">รับสำเนาของข้อมูลคำแนะนำแบบส่วนตัวในรูปแบบดิจิทัล ในนามของผู้ใช้ที่ได้รับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="45138-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="45138-128">ลูกค้าอาจต้องการได้รับสำเนาดิจิตอลของข้อมูลส่วนบุคคลและดูมุมมองที่ส่งออกของผลลัพธ์คำแนะนำนั้น</span><span class="sxs-lookup"><span data-stu-id="45138-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="45138-129">หากลูกค้าร้องขอข้อมูลนี้ ผู้ค้าปลีกจะต้องสร้างส่วนขยายที่กำหนดเองซึ่งเรียกใช้อินเทอร์เฟซการเขียนโปรแกรมประยุกต์เซิร์ฟเวอร์การค้าปลีก (API) และแบบสอบถามสำหรับผลลัพธ์แบบเต็มจากรายการ **เลือกให้คุณ** อิงตามรหัสลูกค้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="45138-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="45138-130">ผลลัพธ์สามารถส่งออกในรูปแบบค่าที่คั่นด้วยเครื่องหมายจุลภาค (CSV) และแบ่งปันไปยังลูกค้า</span><span class="sxs-lookup"><span data-stu-id="45138-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="45138-131">ตัวอย่างต่อไปนี้แสดงวิธีที่ผู้ค้าปลีกสามารถทำงานนี้ให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="45138-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="45138-132">ผู้ค้าปลีกสร้างส่วนขยายที่กำหนดเองเพื่อดึงข้อมูลคำแนะนำแบบส่วนตัวในนามของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="45138-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="45138-133">สำหรับข้อมูลเกี่ยวกับวิธีสร้างโมดูล ลอกแบบโมดูลที่มีอยู่ เรียกเซิร์ฟเวอร์การขายปลีก API และเรียกการดำเนินการข้อมูล โปรดดู [การขยายช่องทางออนไลน์](e-commerce-extensibility/overview.md)</span><span class="sxs-lookup"><span data-stu-id="45138-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="45138-134">ส่วนขยายที่กำหนดเองทำให้การเรียกการดำเนินการข้อมูลหลัก **รับคำแนะนำ** และส่งผ่านข้อมูลที่จำเป็นไปโดยขึ้นอยู่กับความต้องการในรายการ</span><span class="sxs-lookup"><span data-stu-id="45138-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="45138-135">ในกรณีของรายการ **เลือกให้คุณ** ส่วนขยายจะต้องส่งชื่อรายการที่ถูกต้องและรหัสลูกค้าไปยังการดำเนินการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="45138-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="45138-136">วิธีหนึ่งในการสร้างส่วนขยายที่กำหนดเองคือการลอกแบบโมดูลชุดผลิตภัณฑ์ที่มีอยู่ที่ใช้เพื่อส่งคืนผลลัพธ์คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="45138-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="45138-137">ด้วยการลอกแบบโมดูลที่มีอยู่นี้ ผู้ค้าปลีกสามารถแก้ไขรหัสที่มีอยู่และเพิ่มปุ่มใหม่ที่ส่งออกผลลัพธ์คำแนะนำไปยังไฟล์ CSV</span><span class="sxs-lookup"><span data-stu-id="45138-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="45138-138">สำหรับข้อมูลเพิ่มเติม โปรดดู [ลอกแบบโมดูลชุดสินค้าเริ่มต้น](e-commerce-extensibility/clone-starter-module.md) และ [โมดูลชุดผลิตภัณฑ์](product-collection-module-overview.md)</span><span class="sxs-lookup"><span data-stu-id="45138-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="45138-139">สำหรับมุมมองแบบเต็มของไลบรารีเซิร์ฟเวอร์การขายปลีก API ให้ดู [เซิร์ฟเวอร์การขายปลีกลูกค้าและผู้บริโภค API](dev-itpro/retail-server-customer-consumer-api.md)</span><span class="sxs-lookup"><span data-stu-id="45138-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="45138-140">หลังจากสร้างส่วนขยายที่กำหนดเองแล้ว ผู้ค้าปลีกสามารถส่งออกไฟล์ CSV ของผลลัพธ์คำแนะนำทั้งหมด โดยยึดตามรหัสลูกค้าที่ไม่ซ้ำกันของผู้ใช้ที่ได้รับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="45138-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="45138-141">ผู้ค้าปลีกสามารถแชร์ไฟล์ CSV ที่ส่งออกซึ่งมีรายการส่วนบุคคลแบบเต็มของผลิตภัณฑ์ที่แนะนำให้กับผู้ใช้ที่ได้รับการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="45138-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45138-142">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="45138-142">Additional resources</span></span>

[<span data-ttu-id="45138-143">ภาพรวมของคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45138-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="45138-144">เปิดใช้งาน Azure Data Lake Storage ในสภาพแวดล้อม Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="45138-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="45138-145">เปิดใช้งานคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45138-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="45138-146">เปิดใช้งานคำแนะนำที่เป็นแบบส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="45138-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="45138-147">เพิ่มคำแนะนำผลิตภัณฑ์ใน POS</span><span class="sxs-lookup"><span data-stu-id="45138-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="45138-148">เพิ่มคำแนะนำในหน้าจอธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="45138-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="45138-149">ปรับปรุงผลลัพธ์คำแนะนำของ AI-ML</span><span class="sxs-lookup"><span data-stu-id="45138-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="45138-150">สร้างคำแนะนำที่ระบุด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="45138-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="45138-151">สร้างคำแนะนำที่มีข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="45138-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="45138-152">FAQ เกี่ยวกับคำแนะนำผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="45138-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
