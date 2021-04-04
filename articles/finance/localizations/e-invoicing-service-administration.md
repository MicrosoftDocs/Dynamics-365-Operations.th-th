---
title: ส่วนประกอบการดูแลระบบของใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่ม
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับส่วนประกอบที่เกี่ยวข้องกับการจัดการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592585"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="56db5-103">ส่วนประกอบการดูแลระบบของใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="56db5-104">หัวข้อนี้ให้ข้อมูลเกี่ยวกับส่วนประกอบที่เกี่ยวข้องกับการจัดการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="56db5-105">และยังแสดงข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกการให้บริการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="56db5-106">Azure</span><span class="sxs-lookup"><span data-stu-id="56db5-106">Azure</span></span>

<span data-ttu-id="56db5-107">ใช้ Microsoft Azure เพื่อสร้างข้อมูลลับสำหรับที่จัดเก็บหลักและบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="56db5-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="56db5-108">แล้วใช้ข้อมูลลับในการตั้งค่าคอนฟิกของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="56db5-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="56db5-109">Lifecycle Services</span></span>

<span data-ttu-id="56db5-110">ใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อเปิดใช้งานเพิ่มเติมในส่วนของไมโครเซอร์วิสกับโครงการการปรับใช้ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="56db5-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="56db5-111">การติดตั้งไมโครเซอร์วิส Add-on ใน LCS จำเป็นต้องใช้เครื่องเสมือน Tier 2 เป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="56db5-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="56db5-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการวางแผนสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)</span><span class="sxs-lookup"><span data-stu-id="56db5-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="56db5-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="56db5-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="56db5-114">Dynamics 365 Regulatory Configuration Services (RCS) เป็นอินเทอร์เฟซที่ใช้ในการกำหนดค่าคอนฟิกการออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="56db5-115">ทรัพยากร เช่น สภาพแวดล้อมและคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จะถูกสร้าง เก็บรักษา และโฮสต์ใน RCS</span><span class="sxs-lookup"><span data-stu-id="56db5-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="56db5-116">เมื่อทรัพยากรพร้อมแล้ว ก็จะถูกเผยแพร่ไปยังบริการส่วนเพิ่มของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="56db5-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="56db5-117">สำหรับการสมัคร RCS ดูที่ [Regulatory services](https://marketing.configure.global.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="56db5-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="56db5-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCS ดู [Regulatory Configuration Services (RCS) - คุณลักษณะมาตรฐานโลก](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="56db5-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="56db5-119">การใช้งานร่วมกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="56db5-120">ก่อนที่คุณจะสามารถใช้ RCS เพื่อตั้งค่าคอนฟิกใบแจ้งหนี้อิเล็กทรอนิกส์ คุณจะต้องตั้งค่าคอนฟิก RCS เพื่ออนุญาตให้สื่อสารกับ การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="56db5-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="56db5-121">คุณตั้งค่าคอนฟิกนี้ให้สมบูรณ์บนแท็บ **Add-on การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ของหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="56db5-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="56db5-122">ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="56db5-122">Service endpoint</span></span>

<span data-ttu-id="56db5-123">การออกใบแจ้งหนี้อิเล็กทรอนิกส์ Add-on มีให้บริการในพื้นที่ศูนย์ข้อมูล Azure หลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="56db5-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="56db5-124">ตารางต่อไปนี้จะแสดงรายการความพร้อมใช้งานตามภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="56db5-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="56db5-125">ลักษณะของศูนย์ข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="56db5-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="56db5-126">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="56db5-126">East US</span></span>                    |
| <span data-ttu-id="56db5-127">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="56db5-127">West US</span></span>                    |
| <span data-ttu-id="56db5-128">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="56db5-128">North EU</span></span>                   |
| <span data-ttu-id="56db5-129">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="56db5-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="56db5-130">สภาพแวดล้อมของบริการ</span><span class="sxs-lookup"><span data-stu-id="56db5-130">Service environments</span></span>

<span data-ttu-id="56db5-131">สภาพแวดล้อมของบริการคือพาร์ติชันเชิงตรรกะที่สร้างขึ้นเพื่อสนับสนุนการปฏิบัติการคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ในการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="56db5-132">ความลับด้านความปลอดภัยและใบรับรองดิจิทัล และการควบคุม (คือการให้สิทธิการเข้าถึง) ต้องตั้งค่าคอนฟิกที่ระดับสภาพแวดล้อมการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="56db5-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="56db5-133">ลูกค้าสามารถสร้างสภาพแวดล้อมในการให้บริการได้มากเท่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="56db5-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="56db5-134">สภาพแวดล้อมการบริการทั้งหมดที่ลูกค้าสร้างจะไม่ขึ้นต่อกัน</span><span class="sxs-lookup"><span data-stu-id="56db5-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="56db5-135">คุณต้องสร้างและรักษาสภาพแวดล้อมการให้บริการใน RCS</span><span class="sxs-lookup"><span data-stu-id="56db5-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="56db5-136">เมื่อทรัพยากรการให้บริการพร้อมแล้ว ก็จะถูกเผยแพร่ไปยังบริการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="56db5-137">สถานะสภาพแวดล้อมการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="56db5-137">Service environment status</span></span>

<span data-ttu-id="56db5-138">สภาพแวดล้อมการให้บริการสามารถจัดการผ่านสถานะได้</span><span class="sxs-lookup"><span data-stu-id="56db5-138">Service environments can be managed through status.</span></span> <span data-ttu-id="56db5-139">ตัวเลือกที่เป็นไปได้มีดังนี้</span><span class="sxs-lookup"><span data-stu-id="56db5-139">The possible options are:</span></span>

- <span data-ttu-id="56db5-140">**ไมได้เผยแพร่** – สร้างสภาพแวดล้อมแล้ว แต่ยังไม่ได้เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="56db5-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="56db5-141">**เผยแพร่แล้ว** – สภาพแวดล้อมได้รับการเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่มเแล้ว</span><span class="sxs-lookup"><span data-stu-id="56db5-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="56db5-142">**มีการเปลี่ยนแปลง** – แอททริบิวต์ของสภาพแวดล้อมที่เผยแพร่มีการเปลี่ยนแปลง แต่การเปลี่ยนแปลงยังไม่ได้รับการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="56db5-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="56db5-143">ช้อมูลลับของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="56db5-143">Customer secrets</span></span>

<span data-ttu-id="56db5-144">บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่มมีหน้าที่จัดเก็บข้อมูลทางธุรกิจทั้งหมดของคุณในทรัพยากร Azure ที่บริษัทของคุณเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="56db5-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="56db5-145">เพื่อให้แน่ใจว่าการบริการทำงานได้อย่างถูกต้อง และมีการเข้าถึงข้อมูลทางธุรกิจทั้งหมดที่ถูกร้องขอและสร้างขึ้นโดยการออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่มนั้นเข้าถึงได้โดย Add-on เท่านั้น คุณต้องสร้างทรัพยากร Azure หลักสองอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="56db5-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="56db5-146">บัญชีการจัดเก็บของ Azure (Blob storage) ที่จะจัดเก็บใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="56db5-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="56db5-147">Azure Key Vault ที่จะจัดเก็บใบรับรองและตัวระบุทรัพยากรที่เหมือนกัน (URI) ของบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="56db5-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="56db5-148">ต้องมีการจัดสรรที่เก็บข้อมูลหลักและบัญชีการจัดเก็บของลูกค้าโดยเฉพาะเพื่อใช้กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="56db5-149">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="56db5-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="56db5-150">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="56db5-150">Users</span></span>

<span data-ttu-id="56db5-151">สภาพแวดล้อมการบริการแต่ละรายการต้องแสดงรายชื่อผู้ใช้ที่สามารถเชื่อมต่อจาก Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ในการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="56db5-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="56db5-152">การเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="56db5-152">Publication</span></span>

<span data-ttu-id="56db5-153">สภาพแวดล้อมของบริการจะต้องเผยแพร่เพื่อออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่มก่อนที่จะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="56db5-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="56db5-154">เฉพาะสภาพแวดล้อมที่เผยแพร่เท่านั้นที่สามารถเข้าถึงโดย Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="56db5-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="56db5-155">นอกจากนี้ ต้องมีการเผยแพร่สภาพแวดล้อมการบริการก่อนที่การอัพเดตแอททริบิวต์จะมีผลกับบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="56db5-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="56db5-156">แอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="56db5-156">Connected applications</span></span>

<span data-ttu-id="56db5-157">แอพลิเคชันที่เชื่อมต่อคืออินสแตนซ์ของ Finance and Supply Chain Management ที่คุณอาจต้องดำเนินการผ่าน RCS</span><span class="sxs-lookup"><span data-stu-id="56db5-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="56db5-158">นอกจาก URL แอพลิเคชันและผู้เช่าแล้ว แอพลิเคชันที่เชื่อมต่อยังประกอบด้วยข้อมูลอ้างอิงที่ทำให้ RCS สามารถเชื่อมต่อกับสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="56db5-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="56db5-159">คุณสามารถตั้งค่าคอนฟิกส่วนของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Finance and Supply Chain Management เพื่อใช้งานลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ทั้งหมดได้โดยผ่านแอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="56db5-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="56db5-160">Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="56db5-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="56db5-161">การใช้งานร่วมกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="56db5-162">ก่อนที่คุณจะสามารถใช้ Finance and Supply Chain Management เพื่อออกใบแจ้งหนี้อิเล็กทรอนิกส์โดยใช้ Electronic invoicing add-on ต้องตั้งค่าคอนฟิกของบริการส่วนเพิ่มเพื่อให้มีการเชื่อมต่อกับบริการได้</span><span class="sxs-lookup"><span data-stu-id="56db5-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="56db5-163">คุณลักษณะการใช้งานร่วมของการออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="56db5-164">เมื่อต้องการเปิดใช้งานการสื่อสารระหว่างการจัดการด้านการเงินและซัพพลายเชน และการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพ่ิม คุณต้องเปิดใช้คุณลักษณะ **การรวม Add-on การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในพื้นที่ **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="56db5-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="56db5-165">ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="56db5-165">Service endpoint</span></span>

<span data-ttu-id="56db5-166">ปลายทางของบริการคือ URL ที่เป็นที่ตั้งของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="56db5-167">ก่อนที่คุณจะสามารถ ใช้ออกใบแจ้งหนี้อิเล็กทรอนิกส์ได้ ต้องกำหนดค่าคอนฟิกจุดสิ้นสุดในการจัดการด้านการเงินและซัพพลายเชนเพื่อให้สามารถสื่อสารกับบริการได้</span><span class="sxs-lookup"><span data-stu-id="56db5-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="56db5-168">เมื่อต้องการตั้งค่าคอนฟิกปลายทางของบริการ ไปที่ **การจัดการองค์กร \> ตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์** จากนั้น บนแท็บ **บริการการส่ง** ในฟิลด์ **URL ของ Add-on การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ป้อน URL ตามที่อธิบายไว้ในตารางอธิบายในส่วน **จุดสิ้นสุดบริการ**</span><span class="sxs-lookup"><span data-stu-id="56db5-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="56db5-169">สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="56db5-169">Environments</span></span>

<span data-ttu-id="56db5-170">ชื่อของสภาพแวดล้อมที่ป้อนในการจัดการด้านการเงินและซัพพลายเชนหมายถึงชื่อของสภาพแวดล้อมที่สร้างขึ้นใน RCS และเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="56db5-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="56db5-171">ต้องมีการตั้งค่าคอนฟิกของสภาพแวดล้อมบนแท็บ **บริการการส่ง** ของหน้า **พารามิเตอร์เอกสารอิเล็กทรอนิกส์** เพื่อให้ทุกคำขอออกใบแจ้งหนี้อิเล็กทรอนิกส์มีสภาพแวดล้อมที่การออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเพิ่มสามารถกำหนดคุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์ที่ต้องดำเนินการตามคำขอ</span><span class="sxs-lookup"><span data-stu-id="56db5-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56db5-172">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="56db5-172">Additional resources</span></span>

- [<span data-ttu-id="56db5-173">ตั้งค่าคอนฟิกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน RCS</span><span class="sxs-lookup"><span data-stu-id="56db5-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="56db5-174">การออกใบแจ้งหนี้อิเล็กทรอนิกส์ในการเงิน และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="56db5-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
