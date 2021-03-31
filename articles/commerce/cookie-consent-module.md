---
title: โมดูลการยินยอมใช้คุกกี้
description: หัวข้อนี้ครอบคลุมถึงโมดูลการยินยอมใช้คุกกี้และอธิบายวิธีการเพิ่มลงในหน้าไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 57c8876f1faf08ce965ccd796551996a8651e2eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213949"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="de01e-103">โมดูลการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="de01e-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de01e-104">หัวข้อนี้ครอบคลุมถึงโมดูลการยินยอมใช้คุกกี้และอธิบายวิธีการเพิ่มลงในหน้าไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="de01e-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="de01e-105">โมดูลการยินยอมใช้คุกกี้จะแจ้งให้ผู้ใช้เว็บไซต์ให้ความยินยอมอย่างชัดแจ้งเพื่อให้คุกกี้สำหรับคุณลักษณะหรือโมดูลใดๆ ที่ติดตามคุกกี้ของเบราว์เซอร์</span><span class="sxs-lookup"><span data-stu-id="de01e-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="de01e-106">ต้องการความยินยอมในครั้งแรกที่ผู้ใช้ไซต์เรียกดูไซต์ในเซสชันของเบราว์เซอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="de01e-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="de01e-107">เมื่อได้รับความยินยอม จะมีการติดตามและผู้ใช้ไซต์จะไม่ได้รับการแจ้งเตือนสำหรับความยินยอมอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="de01e-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="de01e-108">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปฏิบัติตามข้อกำหนดคุกกี้](cookie-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="de01e-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="de01e-109">ถ้าไม่ได้รับความยินยอมใช้คุกกี้จากผู้ใช้ไซต์ คุณลักษณะหรือโมดูลใดๆ ที่ต้องการความยินยอมใช้คุกกี้จะไม่แสดงขึ้นบนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="de01e-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="de01e-110">ตัวอย่างเช่น โมดูลเช็คเอาท์ โมดูลการแชร์ทางสังคม และคุณลักษณะร้านค้าที่ต้องการทั้งหมดต้องได้รับการยินยอมใช้คุกกี้ และจะไม่แสดงผลถ้าไม่ได้รับความยินยอมจากผู้ใช้ไซต์</span><span class="sxs-lookup"><span data-stu-id="de01e-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="de01e-111">โมดูลการยินยอมใช้คุกกี้สามารถตั้งค่าคอนฟิกในส่วนย่อยของส่วนหัวเพื่อให้สามารถบังคับใช้เมื่อโหลดหน้า</span><span class="sxs-lookup"><span data-stu-id="de01e-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="de01e-112">โมดูลการยินยอมใช้คุกกี้ควรมีข้อความที่ชัดเจนแจ้งให้ผู้ใช้ไซต์ทราบเกี่ยวกับการใช้งานคุ้กกี้บนไซต์และควรระบุลิงก์ไปยังหน้าความเป็นส่วนตัวของไซต์</span><span class="sxs-lookup"><span data-stu-id="de01e-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="de01e-113">ภาพประกอบต่อไปนี้เน้นตัวอย่างของข้อความการยินยอมใช้คุกกี้ที่มีลิงก์ไปยังหน้านโยบายความเป็นส่วนตัวของไซต์ที่แสดงอยู่บนส่วนหัวของหน้าบนไซต์</span><span class="sxs-lookup"><span data-stu-id="de01e-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="de01e-114">![ตัวอย่างของโมดูลการยินยอมใช้คุกกี้](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="de01e-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="de01e-115">คุณสมบัติของโมดูลการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="de01e-115">Cookie consent module properties</span></span>

| <span data-ttu-id="de01e-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="de01e-116">Property name</span></span>             | <span data-ttu-id="de01e-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="de01e-117">Value</span></span>                 | <span data-ttu-id="de01e-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="de01e-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="de01e-119">ข้อความตกแต่ง</span><span class="sxs-lookup"><span data-stu-id="de01e-119">Rich Text</span></span>                  | <span data-ttu-id="de01e-120">ข้อความตกแต่ง</span><span class="sxs-lookup"><span data-stu-id="de01e-120">Rich Text</span></span> | <span data-ttu-id="de01e-121">ระบุการแจ้งเตือนแบบ Rich text กับผู้ใช้ไซต์ที่ไซต์ใช้คุกกี้ของเบราว์เซอร์และผู้ใช้ดังกล่าวควรยอมรับการใช้คุกกี้ของไซต์เพื่อให้สามารถใช้งานไซต์ได้อย่างเต็มประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="de01e-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="de01e-122">ลิงค์</span><span class="sxs-lookup"><span data-stu-id="de01e-122">Links</span></span> | <span data-ttu-id="de01e-123">URL</span><span class="sxs-lookup"><span data-stu-id="de01e-123">URL</span></span> | <span data-ttu-id="de01e-124">คุณสามารถเพิ่มลิงก์หนึ่งรายการขึ้นไปในหน้าความเป็นส่วนตัวของไซต์ที่อธิบายถึงชนิดของคุกกี้ที่ติดตามบนไซต์</span><span class="sxs-lookup"><span data-stu-id="de01e-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="de01e-125">เพิ่มโมดูลการยินยอมใช้คุกกี้ในหน้าของไซต์</span><span class="sxs-lookup"><span data-stu-id="de01e-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="de01e-126">เมื่อต้องการเพิ่มโมดูลการยินยอมใช้คุกกี้ในหน้าของไซต์หลายหน้าได้อย่างมีประสิทธิภาพ อาจเพิ่มลงไปในส่วนย่อยของส่วนหัวของหน้าที่แชร์</span><span class="sxs-lookup"><span data-stu-id="de01e-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="de01e-127">หลังจากที่มีการเพิ่มส่วนย่อยของส่วนหัวในหน้าของไซต์ทั้งหมด การแจ้งเตือนเกี่ยวกับการยินยอมใช้คุกกี้จะมีการแสดงในครั้งแรกที่ผู้ใช้ไซต์นำทางไปยังหน้าใดๆ ของไซต์</span><span class="sxs-lookup"><span data-stu-id="de01e-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="de01e-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับส่วนย่อยและโมดูลของส่วนหัว ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="de01e-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de01e-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="de01e-129">Additional resources</span></span>

[<span data-ttu-id="de01e-130">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="de01e-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="de01e-131">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="de01e-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="de01e-132">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="de01e-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]