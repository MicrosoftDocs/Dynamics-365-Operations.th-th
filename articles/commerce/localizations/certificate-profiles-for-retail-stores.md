---
title: โพรไฟล์ใบรับรองที่ผู้ใช้กำหนดสำหรับร้านค้าปลีก
description: หัวข้อนี้แสดงภาพรวมเกี่ยวกับวิธีใช้ใบรับรองในร้านค้าปลีก
author: josaw
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 66a2cc5c87f5567f0e65842638017e5127d68a13
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798872"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a><span data-ttu-id="3fcb6-103">โพรไฟล์ใบรับรองที่ผู้ใช้กำหนดสำหรับร้านค้าปลีก</span><span class="sxs-lookup"><span data-stu-id="3fcb6-103">User-defined certificate profiles for retail stores</span></span>

[!include [banner](../includes/banner.md)]


## <a name="overview"></a><span data-ttu-id="3fcb6-104">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="3fcb6-104">Overview</span></span>

<span data-ttu-id="3fcb6-105">หัวข้อนี้อธิบายภาพรวมของโพรไฟล์ใบรับรองที่พร้อมใช้งานใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="3fcb6-105">This topic provides an overview of the certificate profiles that are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="3fcb6-106">ฟังก์ชันนี้ขยายคุณลักษณะ [จัดการความลับสำหรับช่องทางการขายปลีก](../dev-itpro/manage-secrets.md) โดยการเพิ่มการสนับสนุนสำหรับใบรับรองเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="3fcb6-106">This functionality extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature by adding support for local certificates.</span></span>

<span data-ttu-id="3fcb6-107">ในขณะที่การขายหน้าร้าน (POS) กำลังรันอยู่ในโหมดออฟไลน์ จะไม่สามารถเข้าถึงใบรับรองที่จัดเก็บอยู่ใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-107">While the point of sale (POS) is running in offline mode, it can't access the certificates that are stored in the key vault.</span></span> <span data-ttu-id="3fcb6-108">ควรใช้ใบรับรองเฉพาะที่แทน</span><span class="sxs-lookup"><span data-stu-id="3fcb6-108">The local certificate should be used instead.</span></span> <span data-ttu-id="3fcb6-109">ระบบสนับสนุนความสามารถต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3fcb6-109">The following capabilities are supported:</span></span>

- <span data-ttu-id="3fcb6-110">การใช้ใบรับรองเฉพาะที่ในสถานการณ์จำลองที่ย้อนกลับ Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-110">Using local certificates in key vault fallback scenarios</span></span>
- <span data-ttu-id="3fcb6-111">การใช้ใบรับรองเฉพาะที่โดยไม่มี Key Vault (ตัวอย่างเช่น ในการติดตั้งในสถานที่)</span><span class="sxs-lookup"><span data-stu-id="3fcb6-111">Using local certificates without a key vault (for example in an on-premises installation)</span></span>
- <span data-ttu-id="3fcb6-112">การอัพเดตในใบรับรองแบบค่อยเป็นค่อยไป มีร้านค้าและเทอร์มินัลบางร้านใช้ใบรับรองรุ่นใหม่ แต่ร้านค้าและเทอร์มินัลอื่นๆ ยังคงใช้รุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3fcb6-112">Gradual update of certificates, where some stores and terminals use a new version of the certificate, but other stores and terminals continue to use the previous version</span></span>

<span data-ttu-id="3fcb6-113">ฟังก์ชันของโพรไฟล์ใบรับรองช่วยให้คุณสามารถระบุใบรับรองเริ่มต้นและตั้งค่าใบสั่งที่ใบรับรองในโพรไฟล์ใบรับรองเดียวกันจะถูกค้นหา</span><span class="sxs-lookup"><span data-stu-id="3fcb6-113">The certificate profiles functionality lets you specify a default certificate and set the order that certificates in the same certificate profile are searched in.</span></span> <span data-ttu-id="3fcb6-114">ฟังก์ชันนี้ยังมีวิธีการตั้งค่าที่คล้ายกันสำหรับใบรับรองเฉพาะที่และใบรับรอง Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-114">This functionality also provides a similar setup approach for local certificates and Key Vault certificates.</span></span> <span data-ttu-id="3fcb6-115">คุณสามารถเพิ่มการตั้งค่าเฉพาะบริษัทสำหรับใบรับรอง แต่จะมีการใช้ตัวระบุข้ามบริษัทเฉพาะสำหรับใบรับรองแต่ละใบในช่องทาง Commerce</span><span class="sxs-lookup"><span data-stu-id="3fcb6-115">You can add company-specific settings for certificates, but the unique cross-company identifier for each certificate can be used in the Commerce channels.</span></span>

### <a name="scenarios"></a><span data-ttu-id="3fcb6-116">สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="3fcb6-116">Scenarios</span></span>

<span data-ttu-id="3fcb6-117">ฟังก์ชันของโพรไฟล์ใบรับรองสนับสนุนสถานการณ์ต่อไปนี้ในช่องทาง Commerce:</span><span class="sxs-lookup"><span data-stu-id="3fcb6-117">The certificate profiles functionality supports the following scenarios in the Commerce channels:</span></span>

- <span data-ttu-id="3fcb6-118">ใช้ใบรับรองเฉพาะที่ในสถานการณ์จำลองที่ย้อนกลับ Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-118">Use a local certificate in key vault fallback scenarios.</span></span> <span data-ttu-id="3fcb6-119">ต่อไปนี้เป็นตัวอย่างของสถานการณ์จำลองย้อนกลับเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="3fcb6-119">Here are some examples of these fallback scenarios:</span></span>

    - <span data-ttu-id="3fcb6-120">ไม่สามารถเข้าถึงพื้นที่เก็บข้อมูลของ Key Vault ได้</span><span class="sxs-lookup"><span data-stu-id="3fcb6-120">The key vault storage isn't accessible.</span></span>
    - <span data-ttu-id="3fcb6-121">ไม่พบใบรับรองในที่เก็บ Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-121">A certificate isn't found in the key vault storage.</span></span>
    - <span data-ttu-id="3fcb6-122">POS กำลังรันอยู่ในโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="3fcb6-122">The POS is running in offline mode.</span></span>

- <span data-ttu-id="3fcb6-123">ใช้ใบรับรองเฉพาะที่ แต่ไม่มีการเก็บใบรับรองใน Key Vault (ตัวอย่างเช่น ในการติดตั้งในสถานที่)</span><span class="sxs-lookup"><span data-stu-id="3fcb6-123">Use local certificates, but without storing them in the key vault (for example, in an on-premises installation).</span></span>
- <span data-ttu-id="3fcb6-124">ทำการปรับปรุงใบรับรองแบบค่อยเป็นค่อยไป ที่ซึ่งใช้ใบรับรองรุ่นใหม่เท่านั้นในร้านค้าหรือบนเทอร์มินัลที่มีรุ่นใหม่พร้อมใช้งานอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="3fcb6-124">Do a gradual update of certificates, where a new version of the certificate is used only in stores or on terminals where the new version is already available.</span></span>
- <span data-ttu-id="3fcb6-125">ใช้ใบรับรองเดียวกันในหลายบริษัท</span><span class="sxs-lookup"><span data-stu-id="3fcb6-125">Use the same certificate in several companies.</span></span>

## <a name="set-up-certificate-profiles"></a><span data-ttu-id="3fcb6-126">การตั้งค่าโพรไฟล์ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-126">Set up certificate profiles</span></span>

<span data-ttu-id="3fcb6-127">กระบวนงานต่อไปนี้อธิบายวิธีการตั้งค่าโพรไฟล์ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-127">The following procedure explains how to set up certificate profiles.</span></span> <span data-ttu-id="3fcb6-128">ก่อนที่คุณจะใช้โพรไฟล์ใบรับรองในช่องทาง Commerce ให้ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3fcb6-128">Before you use certificate profiles in the Commerce channels, follow these steps to configure the settings.</span></span>

1. <span data-ttu-id="3fcb6-129">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เปิดคุณลักษณะ **โพรไฟล์ใบรับรองที่กำหนดโดยผู้ใช้สำหรับร้านค้าปลีก**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-129">In the **Feature management** workspace, turn on the **User-defined certificate profiles for retail stores** feature.</span></span>
2. <span data-ttu-id="3fcb6-130">ไปที่ **การจัดการระบบ \> การตั้งค่า \> โพรไฟล์ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-130">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
3. <span data-ttu-id="3fcb6-131">สร้างเรกคอร์ดและตั้งค่า **โพรไฟล์ใบรับรอง** **ชื่อ** และฟิลด์ **คำอธิบาย** สำหรับใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-131">Create a record, and set the **Certificate profile**, **Name**, and **Description** fields for it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fcb6-132">โพรไฟล์ใบรับรองเป็นตัวระบุเฉพาะของใบรับรองระหว่างบริษัทและส่วนประกอบ Commerce ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3fcb6-132">The certificate profile is a unique identifier of a certificate across all companies and Commerce components.</span></span>

3. <span data-ttu-id="3fcb6-133">บนแท็บ **นิติบุคคล** ให้เพิ่มบรรทัด และเลือกนิติบุคคล (บริษัท) ที่ควรใช้โพรไฟล์ใบรับรองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="3fcb6-133">On the **Legal entities** tab, add a line, and select the legal entity (company) that the current certificate profile should be used for.</span></span> <span data-ttu-id="3fcb6-134">ถ้าควรใช้โพรไฟล์ใบรับรองสำหรับนิติบุคคลหลายราย ให้ทำซ้ำขั้นตอนนี้เพื่อเพิ่มบรรทัดสำหรับแต่ละนิติบุคคลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3fcb6-134">If the certificate profile should be used for multiple legal entities, repeat this step to add a line for each additional legal entity.</span></span>
4. <span data-ttu-id="3fcb6-135">เลือก **การตั้งค่า** เพื่อเปิดหน้า **การตั้งค่าโพรไฟล์ใบรับรอง** ซึ่งคุณสามารถป้อนการตั้งค่าเฉพาะบริษัทสำหรับโพรไฟล์ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-135">Select **Settings** to open the **Certificate profile settings** page, where you can enter company-specific settings for the certificate profile.</span></span>

### <a name="certificate-profile-settings"></a><span data-ttu-id="3fcb6-136">การตั้งค่าโพรไฟล์ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-136">Certificate profile settings</span></span>

<span data-ttu-id="3fcb6-137">เมื่อคุณเลือก **การตั้งค่า** สำหรับบรรทัดโพรไฟล์ใบรับรอง หน้า **การตั้งค่าโพรไฟล์ใบรับรอง** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="3fcb6-137">When you select **Settings** for certificate profile lines, the **Certificate profile settings** page appears.</span></span> <span data-ttu-id="3fcb6-138">หน้านี้จะช่วยให้คุณสามารถระบุว่าจะใช้ใบรับรองใดเมื่อเรียกใช้โพรไฟล์ใบรับรองปัจจุบันในช่องทาง Commerce</span><span class="sxs-lookup"><span data-stu-id="3fcb6-138">This page lets you specify which certificates can be used when the current certificate profile is called in the Commerce channels.</span></span> <span data-ttu-id="3fcb6-139">นอกจากนี้คุณยังสามารถระบุใบสั่งที่ควรใช้ในการค้นหาใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-139">You can also specify the order that certificates should be searched in.</span></span>

> [!NOTE]
> <span data-ttu-id="3fcb6-140">ฟิลด์ **ลำดับความสำคัญ** จะถูกตั้งค่าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3fcb6-140">The **Priority** field is automatically set.</span></span> <span data-ttu-id="3fcb6-141">ค่าของ **1** แสดงถึงระดับความสำคัญสูงสุด</span><span class="sxs-lookup"><span data-stu-id="3fcb6-141">A value of **1** represents the highest priority.</span></span> <span data-ttu-id="3fcb6-142">เมื่อมีการเพิ่มบรรทัดใหม่บนหน้า **การตั้งค่าโพรไฟล์ใบรับรอง** ระดับความสำคัญจะถูกตั้งค่าเป็นหมายเลขที่มากกว่าระดับความสำคัญของบรรทัดก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3fcb6-142">When a new line is added on the **Certificate profile settings** page, its priority is set to a number that is one more than the priority of the previous line.</span></span> <span data-ttu-id="3fcb6-143">เมื่อต้องการเปลี่ยนระดับความสำคัญของบรรทัดที่ระบุ ให้เลือกบรรทัด แล้วเลือก **เลื่อนขึ้น** เพื่อเพิ่มระดับความสำคัญหรือ **เลื่อนลง** เพื่อลดระดับความสำคัญ</span><span class="sxs-lookup"><span data-stu-id="3fcb6-143">To change the priority of a specific line, select the line, and then select either **Move up** to increase the priority or **Move down** to decrease the priority.</span></span>

<span data-ttu-id="3fcb6-144">เมื่อคุณเพิ่มบรรทัดใหม่ลงในหน้า **การตั้งค่าโพรไฟล์ใบรับรอง** ให้ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3fcb6-144">When you add a new line to the **Certificate profile settings** page, set the following fields:</span></span>

- <span data-ttu-id="3fcb6-145">**ชนิดของสถานที่** – เลือกสถานที่เก็บที่มีการจัดเก็บใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-145">**Location type** – Select the location where the certificate is stored.</span></span> <span data-ttu-id="3fcb6-146">ฟิลด์นี้มีค่าที่เป็นไปได้ที่เป็นไปได้สองค่า: **ใบรับรองเฉพาะที่** และ **Key Vault**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-146">This field has two possible values: **Local certificate** and **Key Vault**.</span></span>
- <span data-ttu-id="3fcb6-147">**ใบรับรอง Key Vault** – จำเป็นต้องใช้ฟิลด์นี้ถ้าคุณตั้งค่าฟิลด์ **ชนิดของสถานที่ที่** เป็น **Key Vault**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-147">**Key Vault certificate** – This field is required if you set the **Location type** field to **Key Vault**.</span></span> <span data-ttu-id="3fcb6-148">ใช้เพื่อระบุความลับของใบรับรอง Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-148">Use it to specify a Key Vault certificate secret.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fcb6-149">ก่อนที่คุณจะใช้ใบรับรอง Key Vault ในโพรไฟล์ใบรับรอง ให้ตรวจสอบให้แน่ใจว่าได้อัพโหลดใบรับรองไปยังที่เก็บ Key Vault และทำตามคำแนะนำใน [การตั้งค่าไคลเอนต์ Key Vault ของ Azure](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client)</span><span class="sxs-lookup"><span data-stu-id="3fcb6-149">Before you use a Key Vault certificate in certificate profiles, be sure to upload a certificate to the key vault storage, and follow the instructions in [Set up the Azure Key Vault client](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span></span>

- <span data-ttu-id="3fcb6-150">**ชื่อร้านค้า** – ฟิลด์นี้เป็นฟิลด์ที่ไม่จำเป็นต้องระบุและจะพร้อมใช้งานเฉพาะเมื่อคุณตั้งค่าฟิลด์ **ชนิดสถานที่** เป็น **ใบรับรองเฉพาะที่** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb6-150">**Store name** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="3fcb6-151">ใช้เพื่อระบุชื่อร้านค้าเริ่มต้นที่ควรใช้ในการค้นหาใบรับรองเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="3fcb6-151">Use it to specify a default store name that should be used to search local certificates.</span></span>
- <span data-ttu-id="3fcb6-152">**ที่ตั้งร้านค้า** – ฟิลด์นี้เป็นฟิลด์ที่ไม่จำเป็นต้องระบุและจะพร้อมใช้งานเฉพาะเมื่อคุณตั้งค่าฟิลด์ **ชนิดสถานที่** เป็น **ใบรับรองเฉพาะที่** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb6-152">**Store location** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="3fcb6-153">ใช้เพื่อระบุที่ตั้งร้านค้าเริ่มต้นที่ควรใช้ในการค้นหาใบรับรองเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="3fcb6-153">Use it to specify a default store location that should be used to search local certificates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fcb6-154">ชื่อร้านค้าเริ่มต้นและที่ตั้งร้านค้าจะถูกเพิ่มเพื่อทำให้กระบวนการของการค้นหาใบรับรองเฉพาะที่ใน Commerce Runtime เป็นไปได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="3fcb6-154">The default store name and store location are added to simplify the process of searching local certificates in the Commerce runtime.</span></span> <span data-ttu-id="3fcb6-155">X509StoreProvider มีรายการของโฟลเดอร์ที่จัดเก็บใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-155">X509StoreProvider has a list of folders where certificates are stored.</span></span> <span data-ttu-id="3fcb6-156">ถ้าไม่ได้ระบุชื่อร้านค้าเริ่มต้นและที่ตั้งร้านค้าเริ่มต้น X509StoreProvider จะพยายามค้นหาใบรับรองในโฟลเดอร์อื่นในรายการ</span><span class="sxs-lookup"><span data-stu-id="3fcb6-156">If the default store name and the default store location aren't specified, X509StoreProvider tries to find a certificate in the other folders on its list.</span></span>

- <span data-ttu-id="3fcb6-157">**รหัสประจำตัว** – ฟิลด์นี้เป็นฟิลด์ที่จำเป็นต้องระบุและจะพร้อมใช้งานเฉพาะเมื่อคุณตั้งค่าฟิลด์ **ชนิดสถานที่** เป็น **ใบรับรองเฉพาะที่** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fcb6-157">**Thumbprint** – This field is required and available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="3fcb6-158">ใช้เพื่อระบุรหัสประจำตัวของใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-158">Use it to specify the certificate thumbprint.</span></span>
- <span data-ttu-id="3fcb6-159">**ข้อคิดเห็น** – ฟิลด์นี้ไม่จำเป็นต้องระบุและให้ผู้ใช้ป้อนหมายเหตุ</span><span class="sxs-lookup"><span data-stu-id="3fcb6-159">**Comments** – This field is optional and lets users enter notes.</span></span>

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a><span data-ttu-id="3fcb6-160">ลำดับงาน: กำลังค้นหาใบรับรองใน Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="3fcb6-160">Workflow: Searching certificates in the Commerce runtime</span></span>

<span data-ttu-id="3fcb6-161">ต่อไปนี้เป็นลำดับงานพื้นฐานที่ใช้ในการค้นหาใบรับรองเมื่อมีการเรียกใช้โพรไฟล์ใบรับรองใน Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="3fcb6-161">Here is the basic workflow that is used to search for a certificate when a certificate profile is called in the Commerce runtime.</span></span>

1. <span data-ttu-id="3fcb6-162">ระบบระบุว่าโพรไฟล์ใบรับรองมีการตั้งค่าเฉพาะบริษัทสำหรับนิติบุคคลปัจจุบันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3fcb6-162">The system identifies whether the certificate profile has company-specific settings for the current legal entity.</span></span>
1. <span data-ttu-id="3fcb6-163">ระบบพยายามค้นหาใบรับรองโดยใช้ค่าในหน้า **การตั้งค่าโพรไฟล์ใบรับรอง** สำหรับบรรทัดที่ฟิลด์ **ระดับความสำคัญ** ถูกตั้งค่าเป็น **1**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-163">The system tries to find the certificate by using the values on the **Certificate profile settings** page for the line where the **Priority** field is set to **1**.</span></span>

    - <span data-ttu-id="3fcb6-164">ถ้าฟิลด์ **ชนิดของสถานที่** ถูกตั้งค่าเป็น **Key Vault** ค่าของฟิลด์ **ความลับของใบรับรอง Key Vault** จะใช้ในการค้นหาใบรับรองบนหน้า **พารามิเตอร์ของ Key Vault**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-164">If the **Location type** field is set to **Key Vault**, the value of the **Key Vault certificate secret** field is used to search for the certificate on the **Key vault parameters** page.</span></span> <span data-ttu-id="3fcb6-165">จากนั้นจะมีการค้นหาใบรับรองในที่เก็บ Key Vault</span><span class="sxs-lookup"><span data-stu-id="3fcb6-165">The certificate is then searched for in the key vault storage.</span></span>
    - <span data-ttu-id="3fcb6-166">ถ้าฟิลด์ **ชนิดของสถานที่** ถูกตั้งค่าเป็น **ใบรับรองเฉพาะที่** X509StoreProvider จะค้นหาใบรับรองเป็นอันดับแรก โดยใช้ชื่อร้านค้าและที่ตั้งร้านค้าเริ่มต้น ถ้ามีการระบุพารามิเตอร์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="3fcb6-166">If the **Location type** field is set to **Local certificate**, X509StoreProvider first searches for the certificate by using the default store name and store location, if these parameters are specified.</span></span> <span data-ttu-id="3fcb6-167">แล้วค้นหาในโฟลเดอร์อื่นๆ ทั้งหมดในรายการของโฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="3fcb6-167">It then searches in all other folders on its list of folders.</span></span>

1. <span data-ttu-id="3fcb6-168">ถ้าไม่พบใบรับรอง กระบวนการจะถูกทำซ้ำสำหรับบรรทัดที่ฟิลด์ **ระดับความสำคัญ** ถูกตั้งค่าเป็น **2** และต่อไป</span><span class="sxs-lookup"><span data-stu-id="3fcb6-168">If the certificate isn't found, the process is repeated for the line where the **Priority** field is set to **2**, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="3fcb6-169">ถ้าโพรไฟล์ใบรับรองไม่มีการตั้งค่าสำหรับนิติบุคคลปัจจุบัน หรือถ้าการค้นหาใบรับรองไม่สำเร็จสำหรับบรรทัดทั้งหมดในหน้า **การตั้งค่าโพรไฟล์ใบรับรอง** จะไม่พบใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-169">If the certificate profile has no settings for the current legal entity, or if the certificate search is unsuccessful for all lines on the **Certificate profile settings** page, the certificate isn't found.</span></span>

#### <a name="caching-the-results-of-certificate-searches"></a><span data-ttu-id="3fcb6-170">การแคชผลลัพธ์ของการค้นหาใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-170">Caching the results of certificate searches</span></span>

<span data-ttu-id="3fcb6-171">ผลลัพธ์ของการค้นหาใบรับรองถูกแคช</span><span class="sxs-lookup"><span data-stu-id="3fcb6-171">The results of certificate searches are cached.</span></span> <span data-ttu-id="3fcb6-172">เวลาหมดอายุเริ่มต้นสำหรับแคชเป็นหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-172">The default expiration time for a cache is one hour.</span></span> <span data-ttu-id="3fcb6-173">อย่างไรก็ตาม คุณสามารถปรับแต่งเวลานี้และสามารถตั้งค่าสูงสุดได้ 24 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="3fcb6-173">However, this time can be customized and can be set to a maximum value of 24 hours.</span></span>

### <a name="gradual-update"></a><span data-ttu-id="3fcb6-174">ปรับปรุงแบบค่อยเป็นค่อยไป</span><span class="sxs-lookup"><span data-stu-id="3fcb6-174">Gradual update</span></span>

<span data-ttu-id="3fcb6-175">ถ้ามีการนำใบรับรองรุ่นใหม่ไปใช้ แต่จะไม่สามารถอัพเดตในร้านค้าทั้งหมดในเวลาเดียวกัน ฟังก์ชันของโพรไฟล์ใบรับรองเปิดใช้งานใบรับรองจะถูกอัพเดตแบบค่อยเป็นค่อยไป</span><span class="sxs-lookup"><span data-stu-id="3fcb6-175">If a new version of the certificate is introduced, but it can't be updated in all stores at the same time, the certificate profiles functionality enables the certificate to be updated gradually.</span></span>

1. <span data-ttu-id="3fcb6-176">ค้นหาโพรไฟล์ใบรับรองและบรรทัดที่ควรได้รับการอัพเดต แล้วเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="3fcb6-176">Find a certificate profile and the line that should be updated, and then select **Settings**.</span></span>
1. <span data-ttu-id="3fcb6-177">เพิ่มบรรทัด และระบุการตั้งค่าที่เกี่ยวข้องกับใบรับรองรุ่นล่าสุด</span><span class="sxs-lookup"><span data-stu-id="3fcb6-177">Add a line, and specify settings that are related to the latest version of the certificate.</span></span>
1. <span data-ttu-id="3fcb6-178">เพิ่มค่า **ระดับความสำคัญ** ของบรรทัดใหม่</span><span class="sxs-lookup"><span data-stu-id="3fcb6-178">Increase the **Priority** value of the new line.</span></span> <span data-ttu-id="3fcb6-179">ใช้ปุ่ม **เลื่อนขึ้น** เพื่อเลื่อนบรรทัดเพื่อให้อยู่เหนือบรรทัดสำหรับใบรับรองเดียวกันกับรุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3fcb6-179">Use the **Move up** button to move the line so that it's above the line for the previous version of the same certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="3fcb6-180">ใน Commerce Runtime ใบรับรองรุ่นใหม่จะถูกเรียกก่อน</span><span class="sxs-lookup"><span data-stu-id="3fcb6-180">In the Commerce runtime, the new version of the certificate will be called first.</span></span> <span data-ttu-id="3fcb6-181">ถ้าใบรับรองยังไม่ได้รับการอัพเดตบนร้านค้าหรือบนเทอร์มินัลเฉพาะหนึ่งๆ จะมีการเรียกรุ่นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="3fcb6-181">If the certificate hasn't yet been updated in a specific store or on a specific terminal, the previous version will be called.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]