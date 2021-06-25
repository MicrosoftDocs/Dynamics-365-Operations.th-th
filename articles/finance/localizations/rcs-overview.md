---
title: Regulatory Configuration Service
description: หัวข้อนี้แสดงภาพรวมของความสามารถของ Regulatory Configuration Service (RCS) และอธิบายวิธีการเข้าถึงบริการ
author: JaneA07
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216573"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="f6b4c-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="f6b4c-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6b4c-104">Regulatory Configuration Service (RCS) เป็นโปรแกรมออกแบบแบบสแตนด์อโลนและบริการจัดการวงจรชีวิตสำหรับฟังก์ชันแบบสากลไม่มีรหัส/รหัสต่ำ</span><span class="sxs-lookup"><span data-stu-id="f6b4c-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="f6b4c-105">ผู้มีส่วนได้ส่วนเสียแบบสากลของ RCS ขยายและปรับเปลี่ยนพื้นที่หลักของภาษี การออกใบแจ้งหนี้อิเล็กทรอนิกส์ การรายงานตามระเบียบบังคับ การธนาคาร และเอกสารทางธุรกิจโดยไม่เกี่ยวข้องกับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="f6b4c-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="f6b4c-106">แนวทางแบบสากลไม่มีรหัส/รหัสต่านี้ช่วยให้เป็นสากลง่ายขึ้น เร็วกว่า และต้นทุนที่มีประสิทธิภาพมากกว่าในการสร้างหรือขยาย</span><span class="sxs-lookup"><span data-stu-id="f6b4c-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="f6b4c-107">RCS ให้ความสามารถต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f6b4c-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="f6b4c-108">การสนับสนุนฟังก์ชันทั้งหมดที่ได้รับจากการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="f6b4c-109">เงื่อนไขเบื้องต้นในการตั้งค่าคอนฟิกไมโครเซอร์วิสแบบสากลใหม่</span><span class="sxs-lookup"><span data-stu-id="f6b4c-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="f6b4c-110">สนับสนุนสำหรับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f6b4c-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="f6b4c-111">สำหรับข้อมูลเพิ่มเติม โปรดดู [การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="f6b4c-112">สนับสนุนการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="f6b4c-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="f6b4c-113">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [บริการภาษี](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="f6b4c-114">การสนับสนุนฟังก์ชันคุณลักษณะสากลใหม่ซึ่งช่วยให้การจัดการรอบเวลาของลักษณะการการใช้ฟังก์ชันหลายส่วนประกอบง่ายขึ้น และช่วยให้สามารถตั้งค่าคอนฟิกการการและตั้งค่าพารามิเตอร์ลักษณะการใช้งานต่าง ๆ ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="f6b4c-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="f6b4c-115">หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [Regulatory Configuration Service – การจัดการคุณลักษณะสากลแบบง่ายสำหรับบริการสากล](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="f6b4c-116">สนับสนุนการเผยแพร่ การจัดเก็บ และการแบ่งปันการตั้งค่าคอนฟิกที่กําหนดเองจากส่วนกลางในที่เก็บส่วนกลางเพื่อให้การจัดการการตั้งค่าคอนฟิกง่ายขึ้นโดยไม่ต้องใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="f6b4c-117">การเข้าถึง RCS</span><span class="sxs-lookup"><span data-stu-id="f6b4c-117">Access RCS</span></span>

<span data-ttu-id="f6b4c-118">คุณสามารถลงชื่อสมัครหรือเข้าสู่ระบบ RCS จาก [หน้า Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![ลงชื่อสมัครใช้และลงชื่อเข้าใช้ RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="f6b4c-120">บนหน้า **Regulatory Configuration Service** ให้ตรวจทานและยอมรับข้อกําหนดและเงื่อนไขเพิ่มเติมเพื่อใช้บริการ แล้วเลือกปุ่มใดปุ่มหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f6b4c-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="f6b4c-121">**ลงชื่อสมัคร** หากคุณเป็นผู้ใช้ครั้งแรกของบริการ และคุณใช้ที่อยู่อีเมลธุรกิจเพื่อเตรียมใช้งานสภาพแวดล้อมบริการขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f6b4c-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="f6b4c-122">**เข้าสู่ระบบ** ถ้าคุณเคยลงชื่อสมัครใช้บริการแล้วก่อนหน้านี้ และคุณต้องการเข้าถึงสภาพแวดล้อมขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f6b4c-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="f6b4c-123">ความพร้อมของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="f6b4c-123">Regional availability</span></span>

<span data-ttu-id="f6b4c-124">โดยทั่วไป RCS จะพร้อมใช้งานในภูมิภาคต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f6b4c-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="f6b4c-125">สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="f6b4c-125">United States</span></span>
- <span data-ttu-id="f6b4c-126">อินเดีย</span><span class="sxs-lookup"><span data-stu-id="f6b4c-126">India</span></span>
- <span data-ttu-id="f6b4c-127">ฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="f6b4c-127">France</span></span>
- <span data-ttu-id="f6b4c-128">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="f6b4c-128">Europe</span></span>

<span data-ttu-id="f6b4c-129">ดูรายการภูมิภาคทั้งหมด โปรดดูที่ [Dynamics 365 และ Power Platform: ความพร้อมใช้งาน ที่ตั้งข้อมูล ภาษา และการแปลเป็นภาษาท้องถิ่น](https://aka.ms/dynamics_365_international_availability_deck)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="f6b4c-130">บริษัทเริ่มต้น RCS</span><span class="sxs-lookup"><span data-stu-id="f6b4c-130">RCS default company</span></span>

<span data-ttu-id="f6b4c-131">มีการใช้ฟังก์ชันเวลาการออกแบบที่ใช้ใน RCS ร่วมกันระหว่างบริษัททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f6b4c-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="f6b4c-132">ไม่มีฟังก์ชันเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="f6b4c-132">There is no company-specific functionality.</span></span> <span data-ttu-id="f6b4c-133">ดังนั้น เราขอแนะนำให้ใช้บริษัทหนึ่งแห่ง **DAT** กับสภาพแวดล้อม RCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f6b4c-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="f6b4c-134">อย่างไรก็ตาม ในบางสถานการณ์ คุณอาจต้องการให้รูปแบบ ER ใช้พารามิเตอร์ที่เกี่ยวข้องกับนิติบุคคลหนึ่งๆ</span><span class="sxs-lookup"><span data-stu-id="f6b4c-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="f6b4c-135">ในสถานการณ์เหล่านี้เท่านั้น คุณควรใช้ตัวสลับบริษัทเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f6b4c-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="f6b4c-136">สำหรับตัวอย่าง ให้ดูที่ [ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับนิติบุคคลแต่ละรายการ](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="f6b4c-137">คู่มือ RCS ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-137">Related RCS documentation</span></span>

<span data-ttu-id="f6b4c-138">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับส่วนประกอบที่เกี่ยวข้อง ให้ดูที่หัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f6b4c-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="f6b4c-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="f6b4c-139">**RCS:**</span></span>

    - [<span data-ttu-id="f6b4c-140">สร้างการตั้งค่าคอนฟิก ER ใน RCS และอัปโหลดไปยังที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="f6b4c-141">**ที่เก็บส่วนกลาง:**</span><span class="sxs-lookup"><span data-stu-id="f6b4c-141">**Global repository:**</span></span>

    - [<span data-ttu-id="f6b4c-142">สร้างการตั้งค่าคอนฟิก ER & อัปโหลดไปที่ที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="f6b4c-143">แบ่งปันการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="f6b4c-144">การกรองข้อมูลขั้นสูงในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="f6b4c-145">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="f6b4c-146">ยกเลิกการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="f6b4c-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="f6b4c-147">Regulatory Configuration Service (RCS) – การคิดค่าเสื่อมราคาที่เก็บข้อมูล Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="f6b4c-148">**คุณลักษณะที่ใช้ทั่วโลก**</span><span class="sxs-lookup"><span data-stu-id="f6b4c-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="f6b4c-149">Regulatory configuration service (RCS) - คุณลักษณะที่ใช้ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="f6b4c-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="f6b4c-150">การแก้ไขปัญหาการลงทะเบียน RCS</span><span class="sxs-lookup"><span data-stu-id="f6b4c-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="f6b4c-151">เมื่อคุณลงชื่อสมัครใน RCS จากหน้าบริการ คุณอาจพบปัญหาที่เกี่ยวข้องกับ Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="f6b4c-152">ข้อความแสดงข้อผิดพลาดที่คุณได้รับบ่งชี้ว่าการลงชื่อสมัครใน RCS ปิดอยู่ในขณะนี้ และต้องเปิดอยู่ก่อนที่คุณจะสามารถประมวลผลการลงชื่อสมัครให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="f6b4c-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![ข้อความแสดงข้อผิดพลาดการลงชื่อสมัครใน RCS](media/01_RCSSignUpError.jpg)

<span data-ttu-id="f6b4c-154">ปัญหาเกิดขึ้นเนื่องจากคุณถูกบล็อคไม่ให้ลงชื่อสมัครบอกรับเป็นสมาชิกเฉพาะทาง และต้องเปิดใช้งานคุณสมบัติ `AllowAdHocSubscriptions` ในผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="f6b4c-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="f6b4c-155">หากแผนกไอทีของคุณจัดการผู้เช่าใน Azure ขององค์กร ให้ติดต่อแผนกนั้นเพื่อรายงานปัญหา</span><span class="sxs-lookup"><span data-stu-id="f6b4c-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="f6b4c-156">หากคุณรับผิดชอบการจัดการผู้เช่า Azure ของคุณ คุณสามารถแก้ไขปัญหาโดยการปฏิบัติตามขั้นตอน [การลงชื่อสมัครใช้ระบบบริการ Azure Active Directory ด้วยตนเองคืออะไร](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings)</span><span class="sxs-lookup"><span data-stu-id="f6b4c-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
