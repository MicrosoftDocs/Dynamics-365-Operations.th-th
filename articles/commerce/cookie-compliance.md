---
title: การปฏิบัติตามกฎระเบียบคุกกี้
description: หัวข้อนี้อธิบายถึงข้อควรพิจารณาสำหรับการปฏิบัติตามข้อกำหนดของคุกกี้และนโยบายเริ่มต้นที่รวมอยู่ใน Microsoft Dynamics 365 Commerce
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10a58cf7197d2a8596107a42174b35350e72ae11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215708"
---
# <a name="cookie-compliance"></a><span data-ttu-id="31ab9-103">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="31ab9-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31ab9-104">หัวข้อนี้อธิบายถึงข้อควรพิจารณาสำหรับการปฏิบัติตามข้อกำหนดของคุกกี้และนโยบายเริ่มต้นที่รวมอยู่ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="31ab9-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31ab9-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="31ab9-105">Overview</span></span>

<span data-ttu-id="31ab9-106">ความเป็นส่วนตัวเป็นปัจจัยสำคัญ เมื่อติดตามเทคโนโลยีที่มีผลต่อลูกค้าอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="31ab9-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="31ab9-107">เนื่องจากมาตรฐานการปฏิบัติตามข้อกำหนดด้านความเป็นส่วนตัว เช่น ข้อบังคับทั่วไปเกี่ยวกับการคุ้มครองข้อมูล (GDPR) ในสหภาพยุโรป (EU) จะต้องพิจารณาหลักเกณฑ์ความเป็นส่วนตัวอิเล็กทรอนิกส์สำหรับเว็บไซต์ใดๆ ที่มีการใช้งานอยู่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="31ab9-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="31ab9-108">เนื่องจากไซต์อีคอมเมิร์ซฃจำนวนมากสามารถเข้าถึงได้ทั่วโลกโดยค่าเริ่มต้น คุณจึงควรตรวจสอบมาตรฐานการปฏิบัติตามกฎระเบียบสำหรับไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="31ab9-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="31ab9-109">หากต้องการเรียนรู้เพิ่มเติมเกี่ยวกับหลักการพื้นฐานที่ Microsoft ใช้สำหรับการปฏิบัติตามข้อกำหนดของคุกกี้ ให้ไปที่ [ศูนย์ความเชื่อถือของ Microsoft](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="31ab9-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="31ab9-110">นอกจากนี้คุณยังสามารถรับข้อมูลเพิ่มเติมเกี่ยวกับพื้นที่ของการปฏิบัติตามกฎระเบียบและความเป็นส่วนตัวได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="31ab9-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="31ab9-111">ตารางต่อไปนี้จะแสดงรายการอ้างอิงปัจจุบันของคุกกี้ที่วางโดยไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="31ab9-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="31ab9-112">ชื่อคุกกี้</span><span class="sxs-lookup"><span data-stu-id="31ab9-112">Cookie name</span></span>                               | <span data-ttu-id="31ab9-113">การใช้</span><span class="sxs-lookup"><span data-stu-id="31ab9-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="31ab9-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="31ab9-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="31ab9-115">คุกกี้การตรวจสอบความถูกต้องของ Store Microsoft Azure Active Directory (Azure AD) สำหรับการลงชื่อเข้าใช้ครั้งเดียว (SSO)</span><span class="sxs-lookup"><span data-stu-id="31ab9-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="31ab9-116">จัดเก็บข้อมูลหลักของผู้ใช้ที่เข้ารหัส (ชื่อ นามสกุล อีเมล)</span><span class="sxs-lookup"><span data-stu-id="31ab9-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="31ab9-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="31ab9-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="31ab9-118">รหัสรถเข็นร้านค้าที่ใช้เพื่อดูรายการของผลิตภัณฑ์ที่เพิ่มลงในอินสแตนซ์รถเข็น</span><span class="sxs-lookup"><span data-stu-id="31ab9-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="31ab9-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="31ab9-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="31ab9-120">การติดตามความยินยอมในการปฏิบัติตามกฎระเบียบคุกกี้</span><span class="sxs-lookup"><span data-stu-id="31ab9-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="31ab9-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="31ab9-121">ai_session</span></span>                                  | <span data-ttu-id="31ab9-122">ตรวจสอบจำนวนรอบเวลาของกิจกรรมของผู้ใช้ที่รวมหน้าและคุณลักษณะบางรายการของแอป</span><span class="sxs-lookup"><span data-stu-id="31ab9-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="31ab9-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="31ab9-123">ai_user</span></span>                                     | <span data-ttu-id="31ab9-124">ตรวจสอบจำนวนบุคคลที่ใช้แอปและคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="31ab9-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="31ab9-125">ผู้ใช้จะได้รับการตรวจนับโดยใช้รหัสที่ไม่ระบุชื่อ</span><span class="sxs-lookup"><span data-stu-id="31ab9-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="31ab9-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="31ab9-126">b2cru</span></span>                                       | <span data-ttu-id="31ab9-127">จัดเก็บเปลี่ยนเส้นทาง URL แบบไดนามิก</span><span class="sxs-lookup"><span data-stu-id="31ab9-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="31ab9-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="31ab9-128">JSESSIONID</span></span>                                  | <span data-ttu-id="31ab9-129">ซึ่งใช้โดยตัวเชื่อมต่อการชำระเงิน Adyen เพื่อจัดเก็บรอบเวลาของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="31ab9-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="31ab9-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="31ab9-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="31ab9-131">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="31ab9-131">Authentication</span></span>                                               |
| <span data-ttu-id="31ab9-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="31ab9-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="31ab9-133">ซึ่งใช้สำหรับการรักษาสถานะคำขอ</span><span class="sxs-lookup"><span data-stu-id="31ab9-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="31ab9-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="31ab9-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="31ab9-135">โทเคนการปลอมแปลงคำขอระหว่างไซต์ (CRSF) ที่ใช้เพื่อปกป้องจาก CRSF</span><span class="sxs-lookup"><span data-stu-id="31ab9-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="31ab9-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="31ab9-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="31ab9-137">ซึ่งใช้เพื่อกำหนดเส้นทางคำขอไปยังอินสแตนซ์ของเซิร์ฟเวอร์การตรวจสอบความถูกต้องของการผลิตที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31ab9-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="31ab9-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="31ab9-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="31ab9-139">ซึ่งใช้เพื่อกำหนดเส้นทางคำขอไปยังอินสแตนซ์ของเซิร์ฟเวอร์การตรวจสอบความถูกต้องของการผลิตที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31ab9-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="31ab9-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="31ab9-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="31ab9-141">ซึ่งใช้เพื่อกำหนดเส้นทางคำขอไปยังอินสแตนซ์ของเซิร์ฟเวอร์การตรวจสอบความถูกต้องของการผลิตที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="31ab9-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="31ab9-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="31ab9-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="31ab9-143">ซึ่งใช้สำหรับการรักษารอบเวลา SSO</span><span class="sxs-lookup"><span data-stu-id="31ab9-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="31ab9-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="31ab9-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="31ab9-145">ซึ่งใช้สำหรับการติดตามธุรกรรม (จำนวนของแท็บที่เปิดที่ตรวจสอบความถูกต้องเทียบกับไซต์ธุรกิจ-ผู้บริโภค (B2C)) ซึ่งรวมถึงธุรกรรมปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="31ab9-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="31ab9-146">การยินยอมใช้คุกกี้ของผู้ใช้ไซต์บนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="31ab9-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="31ab9-147">ถ้าคุณลักษณะหรือโมดูลไซต์อีคอมเมิร์ซใช้คุ้กกี้ที่ไม่จำเป็น ต้องได้รับความยินยอมจากผู้ใช้ไซต์ก่อนที่จะมีการติดตามคุกกี้</span><span class="sxs-lookup"><span data-stu-id="31ab9-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="31ab9-148">เมื่อต้องการอนุญาตให้ผู้ใช้ไซต์สามารถให้ความยินยอมใช้คุกกี้บนไซต์อีคอมเมิร์ซ ผู้สร้างไซต์ต้องเพิ่มและตั้งค่าคอนฟิกโมดูลการยินยอมใช้คุกกี้ไว้ในโมดูลการใช้ส่วนหัวของหน้า เพื่อตรวจสอบให้แน่ใจว่ามีการแจ้งและได้รับความยินยอม</span><span class="sxs-lookup"><span data-stu-id="31ab9-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="31ab9-149">ต้องมีการให้ความยินยอมของผู้ใช้ไซต์ก่อนที่คุณลักษณะหรือโมดูลที่ใช้คุ้กกี้ที่ไม่จำเป็นจะสามารถแสดงบนไซต์</span><span class="sxs-lookup"><span data-stu-id="31ab9-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31ab9-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="31ab9-150">Additional resources</span></span>

[<span data-ttu-id="31ab9-151">คุณลักษณะและความสามารถของการช่วยการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="31ab9-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="31ab9-152">ภาพรวมเกี่ยวกับการปฏิบัติตามกฎระเบียบ</span><span class="sxs-lookup"><span data-stu-id="31ab9-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="31ab9-153">เพิ่มหน้านโยบายความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="31ab9-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="31ab9-154">แทนที่รหัสผู้ใช้ที่เชื่อมโยงกับการเปลี่ยนแปลงเนื้อหาที่ติดตาม</span><span class="sxs-lookup"><span data-stu-id="31ab9-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="31ab9-155">โมดูลการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="31ab9-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="31ab9-156">โมดูลส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="31ab9-156">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]