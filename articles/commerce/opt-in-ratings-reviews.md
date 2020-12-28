---
title: เลือกที่จะใช้การให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416137"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="4be3e-103">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="4be3e-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4be3e-104">หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4be3e-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="4be3e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="4be3e-105">Overview</span></span>

<span data-ttu-id="4be3e-106">โซลูชันการให้คะแนนและการตรวจทาน เป็นโซลูชันช่องทาง Omni ที่คุณสามารถทำให้พร้อมใช้งานใน Dynamics 365 Commerce ได้ โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="4be3e-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4be3e-107">LCS เป็นพอร์ทัลการจัดการที่ร้านค้าปลีกใช้ในการจัดการสภาพแวดล้อมของตนเองจากการเตรียมใช้งานเพื่อรื้อถอน</span><span class="sxs-lookup"><span data-stu-id="4be3e-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="4be3e-108">หากคุณต้องการใช้โซลูชันการให้คะแนนและการวิจารณ์บนเว็บไซต์การค้าของคุณ คุณต้องเลือกรับการให้คะแนนและตรวจสอบระหว่างการปรับใช้ไซต์ e-Commerce ของคุณบน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4be3e-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="4be3e-109">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="4be3e-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="4be3e-110">เมื่อต้องการเลือกที่จะใช้การจัดอันดับและข้อคิดเห็นบนไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4be3e-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="4be3e-111">ทำตามขั้นตอนใน [ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="4be3e-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="4be3e-112">ขณะที่คุณยังคงอยู่ใน LCS ให้ไปที่ **ที่การตั้งค่าการปรับใช้การขายปลีก \> การตั้งค่าอื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="4be3e-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="4be3e-113">ตั้งค่าตัวเลือกการ **เปิดใช้งานการจัดอันดับและข้อคิดเห็น** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4be3e-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="4be3e-114">ใน **กลุ่มรักษาความปลอดภัย AAD สำหรับฟิลด์ผู้ควบคุมการการจัดอันดับและแสดงความคิดเห็น** (รหัสออบเจ็กต์ของกลุ่มรักษาความปลอดภัย) ให้ป้อนรหัสของกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) ที่รวมถึงผู้ควบคุมการจัดอันดับและการแสดงความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="4be3e-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![เลือกที่จะใช้การให้คะแนนและบทวิจารณ์](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="4be3e-116">ดำเนินกระบวนการเริ่มต้นทางอีคอมเมิร์ซให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4be3e-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="4be3e-117">หากคุณเป็นลูกค้า Dynamics 365 Commerce แล้ว ซึ่งได้ปรับใช้ไซต์ e-Commerce โดยไม่ต้องเลือกรับการให้คะแนนและการวิจารณ์ และตอนนี้ต้องการใช้การให้คะแนนและการวิจารณ์จากแพคเกจ Dynamics 365 Commerce โปรดส่งคำขอการบริการ</span><span class="sxs-lookup"><span data-stu-id="4be3e-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="4be3e-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการส่งคำขอการบริการ ดู [กระบวนการส่งคำขอการบริการ](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="4be3e-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4be3e-119">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4be3e-119">Additional resources</span></span>

[<span data-ttu-id="4be3e-120">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="4be3e-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="4be3e-121">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="4be3e-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4be3e-122">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="4be3e-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="4be3e-123">ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4be3e-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


