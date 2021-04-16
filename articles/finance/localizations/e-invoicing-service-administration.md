---
title: ส่วนประกอบการจัดการการออกใบแจ้งหนี้อิเล็กทรอนิกส์
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับส่วนประกอบที่เกี่ยวข้องกับการจัดการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840039"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="d02fa-103">ส่วนประกอบการจัดการการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d02fa-104">หัวข้อนี้ให้ข้อมูลเกี่ยวกับส่วนประกอบที่เกี่ยวข้องกับการจัดการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="d02fa-105">นอกจากนี้ ยังแสดงข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกบริการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="d02fa-106">Azure</span><span class="sxs-lookup"><span data-stu-id="d02fa-106">Azure</span></span>

<span data-ttu-id="d02fa-107">ใช้ Microsoft Azure เพื่อสร้างข้อมูลลับสำหรับที่จัดเก็บหลักและบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d02fa-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="d02fa-108">จากนั้น ใช้ข้อมูลลับในการตั้งค่าคอนฟิกของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="d02fa-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d02fa-109">Lifecycle Services</span></span>

<span data-ttu-id="d02fa-110">ใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อเปิดใช้งานไมโครเซอร์วิสสำหรับโครงการการปรับใช้ LCS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d02fa-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="d02fa-111">การติดตั้งไมโครเซอร์วิสใน LCS จำเป็นต้องใช้เครื่องเสมือนระดับ 2 เป็นอย่างน้อย</span><span class="sxs-lookup"><span data-stu-id="d02fa-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="d02fa-112">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการวางแผนสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)</span><span class="sxs-lookup"><span data-stu-id="d02fa-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="d02fa-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="d02fa-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="d02fa-114">Dynamics 365 Regulatory Configuration Services (RCS) เป็นอินเทอร์เฟซที่ถูกใช้ในการตั้งค่าคอนฟิกการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="d02fa-115">ทรัพยากร เช่น สภาพแวดล้อมและคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จะถูกสร้าง เก็บรักษา และโฮสต์ใน RCS</span><span class="sxs-lookup"><span data-stu-id="d02fa-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="d02fa-116">เมื่อทรัพยากรพร้อมแล้ว จะมีการเผยแพร่ไปยังบริการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="d02fa-117">สำหรับการสมัคร RCS ดูที่ [Regulatory services](https://marketing.configure.global.dynamics.com/)</span><span class="sxs-lookup"><span data-stu-id="d02fa-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="d02fa-118">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCS ดู [Regulatory Configuration Services (RCS) - คุณลักษณะมาตรฐานโลก](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="d02fa-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="d02fa-119">การรวมกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="d02fa-120">ก่อนที่คุณจะสามารถใช้ RCS เพื่อตั้งค่าคอนฟิกใบแจ้งหนี้อิเล็กทรอนิกส์ คุณจะต้องตั้งค่าคอนฟิก RCS เพื่ออนุญาตให้การสื่อสารกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="d02fa-121">คุณทำการตั้งค่าคอนฟิกนี้ให้เสร็จสมบูรณ์บนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ของหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="d02fa-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="d02fa-122">ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="d02fa-122">Service endpoint</span></span>

<span data-ttu-id="d02fa-123">การออกใบแจ้งหนี้อิเล็กทรอนิกส์พร้อมใช้งานในภูมิศาสตร์ศูนย์ข้อมูล Azure หลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="d02fa-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="d02fa-124">ตารางต่อไปนี้จะแสดงรายการความพร้อมใช้งานตามภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="d02fa-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="d02fa-125">ลักษณะของศูนย์ข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="d02fa-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="d02fa-126">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="d02fa-126">East US</span></span>                    |
| <span data-ttu-id="d02fa-127">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="d02fa-127">West US</span></span>                    |
| <span data-ttu-id="d02fa-128">EU เหนือ</span><span class="sxs-lookup"><span data-stu-id="d02fa-128">North EU</span></span>                   |
| <span data-ttu-id="d02fa-129">EU ตะวันตก</span><span class="sxs-lookup"><span data-stu-id="d02fa-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="d02fa-130">สภาพแวดล้อมของบริการ</span><span class="sxs-lookup"><span data-stu-id="d02fa-130">Service environments</span></span>

<span data-ttu-id="d02fa-131">สภาพแวดล้อมของบริการคือ พาร์ติชันเชิงตรรกะที่ถูกสร้างขึ้นเพื่อสนับสนุนการปฏิบัติการของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ในการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="d02fa-132">ความลับด้านความปลอดภัยและใบรับรองดิจิทัล และการควบคุม (คือการให้สิทธิการเข้าถึง) ต้องตั้งค่าคอนฟิกที่ระดับสภาพแวดล้อมการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="d02fa-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="d02fa-133">ลูกค้าสามารถสร้างสภาพแวดล้อมในการให้บริการได้มากเท่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d02fa-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="d02fa-134">สภาพแวดล้อมการบริการทั้งหมดที่ลูกค้าสร้างจะไม่ขึ้นต่อกัน</span><span class="sxs-lookup"><span data-stu-id="d02fa-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="d02fa-135">คุณต้องสร้างและรักษาสภาพแวดล้อมการให้บริการใน RCS</span><span class="sxs-lookup"><span data-stu-id="d02fa-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="d02fa-136">เมื่อทรัพยากรบริการพร้อมแล้ว ต้องมีการเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="d02fa-137">สถานะสภาพแวดล้อมการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="d02fa-137">Service environment status</span></span>

<span data-ttu-id="d02fa-138">สภาพแวดล้อมการให้บริการสามารถจัดการผ่านสถานะได้</span><span class="sxs-lookup"><span data-stu-id="d02fa-138">Service environments can be managed through status.</span></span> <span data-ttu-id="d02fa-139">ตัวเลือกที่เป็นไปได้มีดังนี้</span><span class="sxs-lookup"><span data-stu-id="d02fa-139">The possible options are:</span></span>

- <span data-ttu-id="d02fa-140">**ไมได้เผยแพร่** – สร้างสภาพแวดล้อมแล้ว แต่ยังไม่ได้เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d02fa-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="d02fa-141">**เผยแพร่แล้ว** – สภาพแวดล้อมได้รับการเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เแล้ว</span><span class="sxs-lookup"><span data-stu-id="d02fa-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="d02fa-142">**มีการเปลี่ยนแปลง** – แอททริบิวต์ของสภาพแวดล้อมที่เผยแพร่มีการเปลี่ยนแปลง แต่การเปลี่ยนแปลงยังไม่ได้รับการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d02fa-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="d02fa-143">ช้อมูลลับของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="d02fa-143">Customer secrets</span></span>

<span data-ttu-id="d02fa-144">บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์มีหน้าที่จัดเก็บข้อมูลทางธุรกิจทั้งหมดของคุณในทรัพยากร Azure ที่บริษัทของคุณเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="d02fa-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="d02fa-145">เพื่อให้แน่ใจว่าการบริการทำงานได้อย่างถูกต้อง และมีการเข้าถึงข้อมูลทางธุรกิจทั้งหมดที่จำเป็นและถูกสร้างขึ้นโดยการออกใบแจ้งหนี้อิเล็กทรอนิกส์อย่างเหมาะสม คุณต้องสร้างทรัพยากร Azure หลักสองอย่าง:</span><span class="sxs-lookup"><span data-stu-id="d02fa-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="d02fa-146">บัญชีการจัดเก็บของ Azure (Blob storage) ที่จะจัดเก็บใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="d02fa-147">Azure Key Vault ที่จะจัดเก็บใบรับรองและตัวระบุทรัพยากรที่เหมือนกัน (URI) ของบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d02fa-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="d02fa-148">ต้องมีการปันส่วน Key Vault ที่จัดสรรไว้และบัญชีการจัดเก็บของลูกค้า โดยเฉพาะสำหรับการใช้กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="d02fa-149">สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)</span><span class="sxs-lookup"><span data-stu-id="d02fa-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="d02fa-150">ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d02fa-150">Users</span></span>

<span data-ttu-id="d02fa-151">สภาพแวดล้อมการบริการแต่ละรายการต้องแสดงรายชื่อผู้ใช้ที่สามารถเชื่อมต่อจาก Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ในการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="d02fa-152">การเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="d02fa-152">Publication</span></span>

<span data-ttu-id="d02fa-153">สภาพแวดล้อมของบริการจะต้องถูกเผยแพร่ไปยังการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ก่อนที่จะนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="d02fa-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="d02fa-154">เฉพาะสภาพแวดล้อมที่เผยแพร่เท่านั้นที่สามารถเข้าถึงโดย Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d02fa-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="d02fa-155">นอกจากนี้ ต้องมีการเผยแพร่สภาพแวดล้อมการบริการก่อนที่การอัพเดตแอททริบิวต์จะมีผลกับบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="d02fa-156">แอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="d02fa-156">Connected applications</span></span>

<span data-ttu-id="d02fa-157">แอพลิเคชันที่เชื่อมต่อคืออินสแตนซ์ของ Finance and Supply Chain Management ที่คุณอาจต้องดำเนินการผ่าน RCS</span><span class="sxs-lookup"><span data-stu-id="d02fa-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="d02fa-158">นอกจาก URL แอพลิเคชันและผู้เช่าแล้ว แอพลิเคชันที่เชื่อมต่อยังประกอบด้วยข้อมูลอ้างอิงที่ทำให้ RCS สามารถเชื่อมต่อกับสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="d02fa-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="d02fa-159">คุณสามารถตั้งค่าคอนฟิกส่วนของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Finance and Supply Chain Management เพื่อใช้งานลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ทั้งหมดได้โดยผ่านแอพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="d02fa-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="d02fa-160">Finance and Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d02fa-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="d02fa-161">การรวมกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="d02fa-162">ก่อนที่คุณจะสามารถใช้ Finance และ Supply Chain Management เพื่อออกใบแจ้งหนี้อิเล็กทรอนิกส์โดยใช้การออกใบแจ้งหนี้อิเล็กทรอนิกส์ ต้องมีการตั้งค่าคอนฟิกเพื่ออนุญาตให้มีการสื่อสารกับบริการได้</span><span class="sxs-lookup"><span data-stu-id="d02fa-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="d02fa-163">คุณลักษณะการรวมของการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="d02fa-164">เมื่อต้องการเปิดใช้งานการสื่อสารระหว่าง Finance และ Supply Chain Management และการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ คุณต้องเปิดใช้คุณลักษณะ **การรวมการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="d02fa-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="d02fa-165">ปลายทางของบริการ</span><span class="sxs-lookup"><span data-stu-id="d02fa-165">Service endpoint</span></span>

<span data-ttu-id="d02fa-166">ปลายทางของบริการคือ URL ที่เป็นที่ตั้งของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="d02fa-167">ก่อนที่คุณจะสามารถ ใช้ออกใบแจ้งหนี้อิเล็กทรอนิกส์ได้ ต้องกำหนดค่าคอนฟิกจุดสิ้นสุดในการจัดการด้านการเงินและซัพพลายเชนเพื่อให้สามารถสื่อสารกับบริการได้</span><span class="sxs-lookup"><span data-stu-id="d02fa-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="d02fa-168">เมื่อต้องการตั้งค่าคอนฟิกปลายทางของบริการ ไปที่ **การจัดการองค์กร \> ตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์** และจากนั้น บนแท็บ **บริการการส่ง** ในฟิลด์ **URL ของการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ป้อน URL ตามที่อธิบายไว้ในตารางที่อธิบายไว้ในส่วน **ปลายทางของบริการ**</span><span class="sxs-lookup"><span data-stu-id="d02fa-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="d02fa-169">สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d02fa-169">Environments</span></span>

<span data-ttu-id="d02fa-170">ชื่อของสภาพแวดล้อมที่ถูกป้อนใน Finance และ Supply Chain Management หมายถึงชื่อของสภาพแวดล้อมที่ถูกสร้างขึ้นใน RCS และถูกเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d02fa-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="d02fa-171">ต้องมีการตั้งค่าคอนฟิกสภาพแวดล้อมบนแท็บ **บริการการส่ง** ของหน้า **พารามิเตอร์เอกสารอิเล็กทรอนิกส์** เพื่อให้ทุกคำขอเพื่อออกใบแจ้งหนี้อิเล็กทรอนิกส์มีสภาพแวดล้อมที่ซึ่งการออกใบแจ้งหนี้อิเล็กทรอนิกส์สามารถกำหนดคุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์ที่ต้องดำเนินการตามคำขอ</span><span class="sxs-lookup"><span data-stu-id="d02fa-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d02fa-172">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d02fa-172">Additional resources</span></span>

- [<span data-ttu-id="d02fa-173">ตั้งค่าคอนฟิกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน RCS</span><span class="sxs-lookup"><span data-stu-id="d02fa-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="d02fa-174">การออกใบแจ้งหนี้อิเล็กทรอนิกส์ในการเงิน และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d02fa-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
