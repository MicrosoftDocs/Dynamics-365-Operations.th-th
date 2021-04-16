---
title: การปฏิบัติตามกฎระเบียบคุกกี้
description: หัวข้อนี้อธิบายถึงข้อควรพิจารณาสำหรับการปฏิบัติตามข้อกำหนดของคุกกี้และนโยบายเริ่มต้นที่รวมอยู่ใน Microsoft Dynamics 365 Commerce
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796038"
---
# <a name="cookie-compliance"></a><span data-ttu-id="7cde5-103">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="7cde5-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7cde5-104">หัวข้อนี้อธิบายถึงข้อควรพิจารณาสำหรับการปฏิบัติตามข้อกำหนดของคุกกี้และนโยบายเริ่มต้นที่รวมอยู่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7cde5-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7cde5-105">ความเป็นส่วนตัวเป็นปัจจัยสำคัญ เมื่อติดตามเทคโนโลยีที่มีผลต่อลูกค้าอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="7cde5-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="7cde5-106">เนื่องจากมาตรฐานการปฏิบัติตามข้อกำหนดด้านความเป็นส่วนตัว เช่น ข้อบังคับทั่วไปเกี่ยวกับการคุ้มครองข้อมูล (GDPR) ในสหภาพยุโรป (EU) จะต้องพิจารณาหลักเกณฑ์ความเป็นส่วนตัวอิเล็กทรอนิกส์สำหรับเว็บไซต์ใดๆ ที่มีการใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7cde5-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="7cde5-107">เนื่องจากไซต์อีคอมเมิร์ซฃจำนวนมากสามารถเข้าถึงได้ทั่วโลกโดยค่าเริ่มต้น คุณจึงควรตรวจสอบมาตรฐานการปฏิบัติตามกฎระเบียบสำหรับไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="7cde5-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="7cde5-108">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับหลักการพื้นฐานที่ Microsoft ใช้สำหรับการปฏิบัติตามข้อกำหนดของคุกกี้ ให้ไปที่ [ศูนย์ความเชื่อถือของ Microsoft](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="7cde5-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="7cde5-109">นอกจากนี้คุณยังสามารถรับข้อมูลเพิ่มเติมเกี่ยวกับพื้นที่ของการปฏิบัติตามกฎระเบียบและความเป็นส่วนตัวได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="7cde5-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="7cde5-110">ตารางต่อไปนี้จะแสดงรายการอ้างอิงปัจจุบันของคุกกี้ที่วางโดยไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7cde5-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="7cde5-111">ชื่อคุกกี้</span><span class="sxs-lookup"><span data-stu-id="7cde5-111">Cookie name</span></span>                               | <span data-ttu-id="7cde5-112">การใช้</span><span class="sxs-lookup"><span data-stu-id="7cde5-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="7cde5-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="7cde5-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="7cde5-114">คุกกี้การตรวจสอบความถูกต้องของ Store Microsoft Azure Active Directory (Azure AD) สำหรับการลงชื่อเข้าใช้ครั้งเดียว (SSO)</span><span class="sxs-lookup"><span data-stu-id="7cde5-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="7cde5-115">จัดเก็บข้อมูลหลักของผู้ใช้ที่เข้ารหัส (ชื่อ นามสกุล อีเมล)</span><span class="sxs-lookup"><span data-stu-id="7cde5-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="7cde5-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="7cde5-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="7cde5-117">รหัสรถเข็นร้านค้าที่ใช้เพื่อดูรายการของผลิตภัณฑ์ที่เพิ่มลงในอินสแตนซ์รถเข็น</span><span class="sxs-lookup"><span data-stu-id="7cde5-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="7cde5-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="7cde5-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="7cde5-119">การติดตามความยินยอมในการปฏิบัติตามกฎระเบียบคุกกี้</span><span class="sxs-lookup"><span data-stu-id="7cde5-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="7cde5-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="7cde5-120">ai_session</span></span>                                  | <span data-ttu-id="7cde5-121">ตรวจสอบจำนวนรอบเวลาของกิจกรรมของผู้ใช้ที่รวมหน้าและคุณลักษณะบางรายการของแอป</span><span class="sxs-lookup"><span data-stu-id="7cde5-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="7cde5-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="7cde5-122">ai_user</span></span>                                     | <span data-ttu-id="7cde5-123">ตรวจสอบจำนวนบุคคลที่ใช้แอปและคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="7cde5-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="7cde5-124">ผู้ใช้จะได้รับการตรวจนับโดยใช้รหัสที่ไม่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="7cde5-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="7cde5-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="7cde5-125">b2cru</span></span>                                       | <span data-ttu-id="7cde5-126">จัดเก็บเปลี่ยนเส้นทาง URL แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="7cde5-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="7cde5-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="7cde5-127">JSESSIONID</span></span>                                  | <span data-ttu-id="7cde5-128">ซึ่งใช้โดยตัวเชื่อมต่อการชำระเงิน Adyen เพื่อจัดเก็บรอบเวลาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7cde5-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="7cde5-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="7cde5-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="7cde5-130">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="7cde5-130">Authentication</span></span>                                               |
| <span data-ttu-id="7cde5-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="7cde5-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="7cde5-132">ซึ่งใช้สำหรับการรักษาสถานะคำขอ</span><span class="sxs-lookup"><span data-stu-id="7cde5-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="7cde5-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="7cde5-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="7cde5-134">โทเคนการปลอมแปลงคำขอระหว่างไซต์ (CRSF) ที่ใช้เพื่อปกป้องจาก CRSF</span><span class="sxs-lookup"><span data-stu-id="7cde5-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="7cde5-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="7cde5-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="7cde5-136">ซึ่งใช้เพื่อกำหนดเส้นทางคำขอไปยังอินสแตนซ์ของเซิร์ฟเวอร์การตรวจสอบความถูกต้องของการผลิตที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7cde5-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="7cde5-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="7cde5-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="7cde5-138">ซึ่งใช้เพื่อกำหนดเส้นทางคำขอไปยังอินสแตนซ์ของเซิร์ฟเวอร์การตรวจสอบความถูกต้องของการผลิตที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7cde5-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="7cde5-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="7cde5-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="7cde5-140">ซึ่งใช้เพื่อกำหนดเส้นทางคำขอไปยังอินสแตนซ์ของเซิร์ฟเวอร์การตรวจสอบความถูกต้องของการผลิตที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7cde5-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="7cde5-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="7cde5-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="7cde5-142">ซึ่งใช้สำหรับการรักษารอบเวลา SSO</span><span class="sxs-lookup"><span data-stu-id="7cde5-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="7cde5-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="7cde5-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="7cde5-144">ซึ่งใช้สำหรับการติดตามธุรกรรม (จำนวนของแท็บที่เปิดที่ตรวจสอบความถูกต้องเทียบกับไซต์ธุรกิจ-ผู้บริโภค (B2C)) ซึ่งรวมถึงธุรกรรมปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7cde5-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="7cde5-145">การยินยอมใช้คุกกี้ของผู้ใช้ไซต์บนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="7cde5-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="7cde5-146">ถ้าคุณลักษณะหรือโมดูลไซต์อีคอมเมิร์ซใช้คุ้กกี้ที่ไม่จำเป็น ต้องได้รับความยินยอมจากผู้ใช้ไซต์ก่อนที่จะมีการติดตามคุกกี้</span><span class="sxs-lookup"><span data-stu-id="7cde5-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="7cde5-147">เมื่อต้องการอนุญาตให้ผู้ใช้ไซต์สามารถให้ความยินยอมใช้คุกกี้บนไซต์อีคอมเมิร์ซ ผู้สร้างไซต์ต้องเพิ่มและตั้งค่าคอนฟิกโมดูลการยินยอมใช้คุกกี้ไว้ในโมดูลการใช้ส่วนหัวของหน้า เพื่อตรวจสอบให้แน่ใจว่ามีการแจ้งและได้รับความยินยอม</span><span class="sxs-lookup"><span data-stu-id="7cde5-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="7cde5-148">ต้องมีการให้ความยินยอมของผู้ใช้ไซต์ก่อนที่คุณลักษณะหรือโมดูลที่ใช้คุ้กกี้ที่ไม่จำเป็นจะสามารถแสดงบนไซต์</span><span class="sxs-lookup"><span data-stu-id="7cde5-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7cde5-149">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7cde5-149">Additional resources</span></span>

[<span data-ttu-id="7cde5-150">คุณลักษณะและความสามารถของการช่วยการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="7cde5-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="7cde5-151">ภาพรวมเกี่ยวกับการปฏิบัติตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="7cde5-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="7cde5-152">เพิ่มหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="7cde5-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="7cde5-153">แทนที่รหัสผู้ใช้ที่เชื่อมโยงกับการเปลี่ยนแปลงเนื้อหาที่ติดตาม</span><span class="sxs-lookup"><span data-stu-id="7cde5-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="7cde5-154">โมดูลการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="7cde5-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="7cde5-155">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="7cde5-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
