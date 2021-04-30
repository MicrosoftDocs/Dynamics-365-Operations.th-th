---
title: Regulatory Configuration Service
description: หัวข้อนี้แสดงภาพรวมของความสามารถของ Regulatory Configuration Service (RCS) และอธิบายวิธีการเข้าถึงบริการ
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
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
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890811"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="1b038-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="1b038-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b038-104">Regulatory Configuration Service (RCS) เป็นโปรแกรมออกแบบแบบสแตนด์อโลนและบริการจัดการวงจรชีวิตสำหรับฟังก์ชันแบบสากลไม่มีรหัส/รหัสต่ำ</span><span class="sxs-lookup"><span data-stu-id="1b038-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="1b038-105">ผู้มีส่วนได้ส่วนเสียแบบสากลของ RCS ขยายและปรับเปลี่ยนพื้นที่หลักของภาษี การออกใบแจ้งหนี้อิเล็กทรอนิกส์ การรายงานตามระเบียบบังคับ การธนาคาร และเอกสารทางธุรกิจโดยไม่เกี่ยวข้องกับนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="1b038-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="1b038-106">แนวทางแบบสากลไม่มีรหัส/รหัสต่านี้ช่วยให้เป็นสากลง่ายขึ้น เร็วกว่า และต้นทุนที่มีประสิทธิภาพมากกว่าในการสร้างหรือขยาย</span><span class="sxs-lookup"><span data-stu-id="1b038-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="1b038-107">RCS ให้ความสามารถต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1b038-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="1b038-108">การสนับสนุนฟังก์ชันทั้งหมดที่ได้รับจากการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="1b038-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="1b038-109">เงื่อนไขเบื้องต้นในการตั้งค่าคอนฟิกไมโครเซอร์วิสแบบสากลใหม่</span><span class="sxs-lookup"><span data-stu-id="1b038-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="1b038-110">สนับสนุนสำหรับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1b038-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="1b038-111">สำหรับข้อมูลเพิ่มเติม โปรดดู [การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)</span><span class="sxs-lookup"><span data-stu-id="1b038-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="1b038-112">สนับสนุนการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="1b038-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="1b038-113">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [บริการภาษี](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)</span><span class="sxs-lookup"><span data-stu-id="1b038-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="1b038-114">การสนับสนุนฟังก์ชันคุณลักษณะสากลใหม่ซึ่งช่วยให้การจัดการรอบเวลาของลักษณะการการใช้ฟังก์ชันหลายส่วนประกอบง่ายขึ้น และช่วยให้สามารถตั้งค่าคอนฟิกการการและตั้งค่าพารามิเตอร์ลักษณะการใช้งานต่าง ๆ ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="1b038-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="1b038-115">หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [Regulatory Configuration Service – การจัดการคุณลักษณะสากลแบบง่ายสำหรับบริการสากล](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)</span><span class="sxs-lookup"><span data-stu-id="1b038-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="1b038-116">สนับสนุนการเผยแพร่ การจัดเก็บ และการแบ่งปันการตั้งค่าคอนฟิกที่กําหนดเองจากส่วนกลางในที่เก็บส่วนกลางเพื่อให้การจัดการการตั้งค่าคอนฟิกง่ายขึ้นโดยไม่ต้องใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="1b038-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="1b038-117">การเข้าถึง RCS</span><span class="sxs-lookup"><span data-stu-id="1b038-117">Access RCS</span></span>

<span data-ttu-id="1b038-118">คุณสามารถลงชื่อสมัครหรือเข้าสู่ระบบ RCS จาก [หน้า Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="1b038-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![ลงชื่อสมัครใช้และลงชื่อเข้าใช้ RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="1b038-120">บนหน้า **Regulatory Configuration Service** ให้ตรวจทานและยอมรับข้อกําหนดและเงื่อนไขเพิ่มเติมเพื่อใช้บริการ แล้วเลือกปุ่มใดปุ่มหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1b038-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="1b038-121">**ลงชื่อสมัคร** หากคุณเป็นผู้ใช้ครั้งแรกของบริการ และคุณใช้ที่อยู่อีเมลธุรกิจเพื่อเตรียมใช้งานสภาพแวดล้อมบริการขององค์กร</span><span class="sxs-lookup"><span data-stu-id="1b038-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="1b038-122">**เข้าสู่ระบบ** ถ้าคุณเคยลงชื่อสมัครใช้บริการแล้วก่อนหน้านี้ และคุณต้องการเข้าถึงสภาพแวดล้อมขององค์กร</span><span class="sxs-lookup"><span data-stu-id="1b038-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="1b038-123">ความพร้อมของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="1b038-123">Regional availability</span></span>

<span data-ttu-id="1b038-124">โดยทั่วไป RCS จะพร้อมใช้งานในภูมิภาคต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1b038-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="1b038-125">สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="1b038-125">United States</span></span>
- <span data-ttu-id="1b038-126">อินเดีย</span><span class="sxs-lookup"><span data-stu-id="1b038-126">India</span></span>
- <span data-ttu-id="1b038-127">ฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="1b038-127">France</span></span>
- <span data-ttu-id="1b038-128">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="1b038-128">Europe</span></span>

<span data-ttu-id="1b038-129">ดูรายการภูมิภาคทั้งหมด โปรดดูที่ [Dynamics 365 และ Power Platform: ความพร้อมใช้งาน ที่ตั้งข้อมูล ภาษา และการแปลเป็นภาษาท้องถิ่น](https://aka.ms/dynamics_365_international_availability_deck)</span><span class="sxs-lookup"><span data-stu-id="1b038-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="1b038-130">คู่มือ RCS ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="1b038-130">Related RCS documentation</span></span>

<span data-ttu-id="1b038-131">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับส่วนประกอบที่เกี่ยวข้อง ให้ดูที่คู่มือต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1b038-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="1b038-132">**ที่เก็บส่วนกลาง:**</span><span class="sxs-lookup"><span data-stu-id="1b038-132">**Global repository:**</span></span>

    - [<span data-ttu-id="1b038-133">สร้างการตั้งค่าคอนฟิก ER & อัปโหลดไปที่ที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="1b038-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="1b038-134">แบ่งปันการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="1b038-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="1b038-135">การกรองข้อมูลขั้นสูงในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="1b038-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="1b038-136">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="1b038-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="1b038-137">ยกเลิกการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="1b038-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="1b038-138">**คุณลักษณะที่ใช้ทั่วโลก**</span><span class="sxs-lookup"><span data-stu-id="1b038-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="1b038-139">Regulatory configuration service (RCS) - คุณลักษณะที่ใช้ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="1b038-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)