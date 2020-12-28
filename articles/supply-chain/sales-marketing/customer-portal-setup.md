---
title: ติดตั้ง ตั้งค่า และอัพเดทพอร์ทัลของลูกค้า
description: หัวข้อนี้แสดงรายละเอียดของการให้สิทธิ์ใช้งาน และคำแนะนำการตั้งค่าสำหรับพอร์ทัลลูกค้า
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529541"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="9a45c-103">ติดตั้ง ตั้งค่า และอัพเดทพอร์ทัลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9a45c-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="9a45c-104">ข้อกำหนดสิทธิใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9a45c-104">Licensing requirements</span></span>

<span data-ttu-id="9a45c-105">เมื่อต้องการใช้งานพอร์ทัลลูกค้า คุณต้องมีสิทธิ์ใช้งานดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9a45c-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="9a45c-106">**พอร์ทัล Power Apps** – สิทธิ์การใช้งานนี้จำเป็นต้องใช้เพื่อโฮสต์พอร์ทัลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9a45c-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="9a45c-107">พอร์ทัลจะได้รับสิทธิ์ใช้งานตามการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="9a45c-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="9a45c-108">สำหรับข้อมูลเพิ่มเติม ดูที่ [พอร์ทัล Power Apps ข้อกำหนดสิทธิใช้งาน](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals)</span><span class="sxs-lookup"><span data-stu-id="9a45c-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="9a45c-109">**การรวมแบบสองทิศทาง** – คุณต้องมีสิทธิ์การใช้งานที่จำเป็นเพื่อเปิดใช้งานการรวมแบบสองทิศทาง สำหรับเอนทิตี้ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="9a45c-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="9a45c-110">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ความต้องการของระบบสำหรับการรวมแบบสองทิศทาง](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)</span><span class="sxs-lookup"><span data-stu-id="9a45c-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="9a45c-111">การดำเนินการที่ขึ้นกับการรวมแบบสองทิศทาง และพอร์ทัล Power Apps</span><span class="sxs-lookup"><span data-stu-id="9a45c-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="9a45c-112">พอร์ทัลลูกค้าจะขึ้นอยู่กับพอร์ทัล Power Apps และการรวมแบบสองทิศทาง ดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9a45c-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="9a45c-113">![ความเชื่อมโยงของพอร์ทัลลูกค้า](media/customer-portal-elements.png "ความเชื่อมโยงของพอร์ทัลลูกค้า")</span><span class="sxs-lookup"><span data-stu-id="9a45c-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="9a45c-114">ซึ่งแตกต่างจากลักษณะการทำงานอื่น ๆ จาก Supply Chain Management แม่แบบพอร์ทัลลูกค้าจะอยู่ในพอร์ทัล Power Apps</span><span class="sxs-lookup"><span data-stu-id="9a45c-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="9a45c-115">เพราะฉะนั้น พอร์ทัลลูกค้าจะถูกจำกัดโดยฟังก์ชัน และความสามารถที่มาจากพอร์ทัล Power Apps และเอนทิตี้ในการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="9a45c-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a> <span data-ttu-id="9a45c-116">การตั้งค่าที่จำเป็นเพื่อเปิดใช้งานพอร์ทัลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9a45c-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="9a45c-117">หลังจากที่คุณตรวจสอบให้แน่ใจว่าคุณมีสิทธิใช้งานแล้ว จำเป็นคุณสามารถตั้งค่าการรวมแบบสองทิศทาง ตามที่อธิบายไว้ใน [คำแนะนำการซิงโครไนส์เริ่มต้นของการรวมแบบสองทิศทาง](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md)</span><span class="sxs-lookup"><span data-stu-id="9a45c-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="9a45c-118">ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการแม็ปเอนทิตี้ต่อไปนี้ในการรวมแบบสองทิศทาง:</span><span class="sxs-lookup"><span data-stu-id="9a45c-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="9a45c-119">ส่วนหัวของใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="9a45c-119">Sales Order Header</span></span>
- <span data-ttu-id="9a45c-120">รายละเอียดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="9a45c-120">Sales Order Details</span></span>
- <span data-ttu-id="9a45c-121">บัญชี</span><span class="sxs-lookup"><span data-stu-id="9a45c-121">Accounts</span></span>
- <span data-ttu-id="9a45c-122">ผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="9a45c-122">Contacts</span></span>
- <span data-ttu-id="9a45c-123">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9a45c-123">Products</span></span>

<span data-ttu-id="9a45c-124">หลังจากที่การตั้งค่านี้เสร็จสมบูรณ์ คุณสามารถจัดเตรียมแม่แบบพอร์ทัลลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="9a45c-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="9a45c-125">การจัดเตรียมพอร์ทัลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9a45c-125">Provision the Customer portal</span></span>

<span data-ttu-id="9a45c-126">ก่อนที่คุณจะเริ่มต้น โปรดตรวจสอบให้แน่ใจว่าคุณได้ทำการ [ตั้งค่าที่จำเป็น](#required-setup) เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="9a45c-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="9a45c-127">ให้ทำตามขั้นตอนต่อไปนี้เพื่อจัดเตรียมพอร์ทัลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9a45c-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="9a45c-128">ไปที่ [make.powerapps.com](https://make.powerapps.com/)</span><span class="sxs-lookup"><span data-stu-id="9a45c-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="9a45c-129">ตรวจสอบให้แน่ใจว่าคุณกำลังใช้สภาพแวดล้อมที่คุณเปิดใช้งานการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="9a45c-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="9a45c-130">บนแท็บ **สร้าง** เลื่อนลงไปที่ส่วน **เริ่มต้นจากเท็มเพลต** และเลือกเท็มเพลตที่มีชื่อว่า **พอร์ทัลของลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="9a45c-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="9a45c-131">ทำตามคำแนะนำบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="9a45c-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="9a45c-132">หลังจากการเตรียมเสร็จสมบูรณ์ แล้วคุณสามารถเข้าถึงพอร์ทัลของลูกค้าในส่วน **แอปของคุณ** จาก **โฮม** เพจ</span><span class="sxs-lookup"><span data-stu-id="9a45c-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="9a45c-133">ถ้าไม่ได้ติดตั้งโซลูชันการรวมแบบสองทิศทางในสภาพแวดล้อมที่คุณกำลังทำงานอยู่ คุณจะได้รับข้อความแสดงข้อผิดพลาดและไม่สามารถเตรียมใช้งานพอร์ทัลของลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="9a45c-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="9a45c-134">อัพเดทพอร์ทัลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9a45c-134">Update the Customer portal</span></span>

<span data-ttu-id="9a45c-135">ฟังก์ชันเพิ่มเติมอาจถูกเพิ่มเข้าในพอร์ทัลลูกค้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9a45c-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="9a45c-136">การเปลี่ยนแปลงใด ๆ ที่ Microsoft ทำกับส่วนประกอบของโซลูชันพื้นฐาน จะปรากฏในสภาพแวดล้อมของคุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9a45c-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="9a45c-137">อย่างไรก็ตาม เว็บไซต์ที่กำลังเตรียมใช้งานในสภาพแวดล้อมของคุณ จะไม่สะท้อนถึงการเปลี่ยนแปลงที่เกิดขึ้นกับข้อมูลการตั้งค่าคอนฟิกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9a45c-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="9a45c-138">คุณจะต้องใช้การเปลี่ยนแปลงดังกล่าวด้วยตนเอง โดยการรับโค้ดจากแม่แบบใหม่และรวมกับเว็บไซต์ที่ถูกเตรียมแล้ว</span><span class="sxs-lookup"><span data-stu-id="9a45c-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a45c-139">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9a45c-139">Additional resources</span></span>

<span data-ttu-id="9a45c-140">เมื่อต้องการเรียนรู้ว่าคุณสามารถตั้งค่าและกำหนดค่าพอร์ทัลของลูกค้าเองได้อย่างไร คุณควรเริ่มต้นด้วยการดูเอกสารประกอบต่อไปนี้สำหรับเทคโนโลยีพื้นฐานดังนี้</span><span class="sxs-lookup"><span data-stu-id="9a45c-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="9a45c-141">เอกสารพอร์ทัล Power Apps</span><span class="sxs-lookup"><span data-stu-id="9a45c-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="9a45c-142">เอกสารการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="9a45c-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="9a45c-143">ในการจัดการพอร์ทัลของคุณอย่างมีประสิทธิภาพ คุณต้องเข้าใจพอร์ทัล Power Apps และวงจรของ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9a45c-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="9a45c-144">สำหรับข้อมูลเพิ่มเติม ให้ดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9a45c-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="9a45c-145">เกี่ยวกับวงจรชีวิตของพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="9a45c-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="9a45c-146">อัพเกรดพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="9a45c-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="9a45c-147">ย้ายการตั้งค่าคอนฟิกพอร์ทัล</span><span class="sxs-lookup"><span data-stu-id="9a45c-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="9a45c-148">Solution Lifecycle Management: แอป Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="9a45c-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
