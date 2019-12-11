---
title: เลือกที่จะใช้การให้คะแนนและบทวิจารณ์
description: หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697991"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="53a3f-103">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="53a3f-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="53a3f-104">หัวข้อนี้จะอธิบายถึงวิธีการเลือกที่จะใช้การจัดอันดับและแสดงความคิดเห็นบนไซต์ Microsoft Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="53a3f-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="53a3f-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="53a3f-105">Overview</span></span>

<span data-ttu-id="53a3f-106">โซลูชันการจัดอันดับและข้อคิดเห็นคือโซลูชันช่องทาง omni ที่คุณสามารถทำให้พร้อมใช้งานใน Dynamics 365 Commerce โดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="53a3f-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="53a3f-107">LCS เป็นพอร์ทัลการจัดการที่ร้านค้าปลีกใช้ในการจัดการสภาพแวดล้อมของตนเองจากการเตรียมใช้งานเพื่อรื้อถอน</span><span class="sxs-lookup"><span data-stu-id="53a3f-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="53a3f-108">ถ้าคุณต้องการใช้การจัดอันดับและโซลูชันข้อคิดเห็นบนเว็บไซต์การค้าของคุณ คุณต้องเลือกที่จะเข้าร่วมก่อน</span><span class="sxs-lookup"><span data-stu-id="53a3f-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="53a3f-109">เลือกที่จะใช้การให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="53a3f-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="53a3f-110">เมื่อต้องการเลือกที่จะใช้การจัดอันดับและข้อคิดเห็นบนไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="53a3f-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="53a3f-111">ทำตามขั้นตอนใน [ปรับใช้ไซต์อีคอมเมิร์ซใหม่](deploy-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="53a3f-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="53a3f-112">ขณะที่คุณยังคงอยู่ใน LCS ให้ไปที่ **ที่การตั้งค่าการปรับใช้การขายปลีก \> การตั้งค่าอื่นๆ**</span><span class="sxs-lookup"><span data-stu-id="53a3f-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="53a3f-113">ตั้งค่าตัวเลือกการ **เปิดใช้งานการจัดอันดับและข้อคิดเห็น** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="53a3f-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="53a3f-114">ใน **กลุ่มรักษาความปลอดภัย AAD สำหรับฟิลด์ผู้ควบคุมการการจัดอันดับและแสดงความคิดเห็น** (รหัสออบเจ็กต์ของกลุ่มรักษาความปลอดภัย) ให้ป้อนรหัสของกลุ่มรักษาความปลอดภัยของ Microsoft Azure Active Directory (Azure AD) ที่รวมถึงผู้ควบคุมการจัดอันดับและการแสดงความคิดเห็น</span><span class="sxs-lookup"><span data-stu-id="53a3f-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![เลือกที่จะใช้การให้คะแนนและบทวิจารณ์](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="53a3f-116">ดำเนินกระบวนการเริ่มต้นทางอีคอมเมิร์ซให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="53a3f-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53a3f-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="53a3f-117">Additional resources</span></span>

[<span data-ttu-id="53a3f-118">ภาพรวมของการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="53a3f-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="53a3f-119">จัดการการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="53a3f-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="53a3f-120">ตั้งค่าคอนฟิกการให้คะแนนและบทวิจารณ์</span><span class="sxs-lookup"><span data-stu-id="53a3f-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="53a3f-121">ซิงค์การจัดอันดับผลิตภัณฑ์ใน Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="53a3f-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
