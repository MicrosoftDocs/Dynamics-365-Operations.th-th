---
title: สร้างบัญชีการจัดเก็บของ Azure และ Key Vault
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างบัญชีการจัดเก็บของ Azure และ Key Vault
author: gionoder
ms.date: 02/12/2021
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
ms.openlocfilehash: 2786d350fde2399aadb35dc653bc15123e0e6d91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893813"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="4fe35-103">สร้างบัญชีการจัดเก็บของ Azure และ Key Vault</span><span class="sxs-lookup"><span data-stu-id="4fe35-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4fe35-104">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4fe35-104">Prerequisites</span></span>

<span data-ttu-id="4fe35-105">ก่อนที่คุณจะสามารถทำขั้นตอนต่างๆ ให้เสร็จสมบูรณ์ในหัวข้อนี้ คุณต้องแน่ใจว่างานต่อไปนี้ได้เสร็จสมบูรณ์แล้ว:</span><span class="sxs-lookup"><span data-stu-id="4fe35-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="4fe35-106">สร้างทรัพยากร Key Vault ใน Azure</span><span class="sxs-lookup"><span data-stu-id="4fe35-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="4fe35-107">สำหรับข้อมูลเพิ่มเติม ให้ดู [About Azure Key Vault](/azure/key-vault/general/overview)</span><span class="sxs-lookup"><span data-stu-id="4fe35-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="4fe35-108">สร้างบัญชีการจัดเก็บของ Azure (ที่จัดเก็บ Blob)</span><span class="sxs-lookup"><span data-stu-id="4fe35-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="4fe35-109">สำหรับข้อมูลเพิ่มเติม ให้ดู [Maintaining Azure Storage Account](/azure/storage/blobs/)</span><span class="sxs-lookup"><span data-stu-id="4fe35-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="4fe35-110">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="4fe35-110">Overview</span></span>

<span data-ttu-id="4fe35-111">ในหัวข้อนี้ คุณจะดำเนินการขั้นตอนหลักสองขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4fe35-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="4fe35-112">ตั้งค่าบัญชีการจัดเก็บของ Azure เพื่อให้ได้ URI บัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4fe35-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="4fe35-113">ตั้งค่า Key Vault สำหรับจัดเก็บ URI ของบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4fe35-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="4fe35-114">ตั้งค่าบัญชีการจัดเก็บของ Azure เพื่อให้ได้ URI ของบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4fe35-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="4fe35-115">เปิดบัญชีจัดการเก็บที่คุณวางแผนที่จะใช้กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4fe35-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="4fe35-116">ไปที่ **บริการ Blob** \> **คอนเทนเนอร์** และสร้างคอนเทนเนอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="4fe35-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="4fe35-117">ป้อนชื่อสำหรับคอนเทนเนอร์ และตั้งค่าฟิลด์ **ระดับการเข้าถึงสาธารณะ** เป็น **ส่วนตัว (ไม่มีการเข้าถึงแบบไม่ระบุชื่อ)**</span><span class="sxs-lookup"><span data-stu-id="4fe35-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="4fe35-118">เปิดคอนเทนเนอร์ และไปที่ **การตั้งค่า \> นโยบายการเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="4fe35-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="4fe35-119">เลือก **เพิ่มนโยบาย** เพื่อเพิ่มนโยบายการเข้าถึงการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4fe35-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="4fe35-120">ตั้งค่าฟิลด์ **ตัวระบุ** และ **สิทธิ์** ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="4fe35-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="4fe35-121">ในฟิลด์ **สิทธิ์** คุณควรเลือกสิทธิ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4fe35-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![สิทธิ์การจัดเก็บ Granting Blob](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="4fe35-123">ป้อนวันที่เริ่มต้นและวันที่หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="4fe35-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="4fe35-124">วันหมดอายุควรอยู่ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="4fe35-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="4fe35-125">เลือก **ตกลง** เพื่อบันทึกนโยบาย แล้วบันทึกการเปลี่ยนแปลงของคุณไปยังคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="4fe35-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="4fe35-126">กลับไปยังบัญชีการจัดเก็บ และเปิด **Storage Explorer (การแสดงตัวอย่าง)**</span><span class="sxs-lookup"><span data-stu-id="4fe35-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="4fe35-127">คลิกขวาที่คอนเทนเนอร์ แล้วเลือก **รับลายเซ็นที่ใช้การเข้าถึงร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="4fe35-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="4fe35-128">ในกล่องโต้ตอบ **ลายเซ็นที่ใช้การเข้าถึงร่วมกัน** ให้คัดลอกและจัดเก็บค่าในฟิลด์ **URI**</span><span class="sxs-lookup"><span data-stu-id="4fe35-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="4fe35-129">ค่านี้จะใช้ในขั้นตอนถัดไป และจะถูกเรียกว่า *URI ลายเซ็นที่ใช้การเข้าถึงร่วมกัน*</span><span class="sxs-lookup"><span data-stu-id="4fe35-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![การเลือกและการคัดลอกค่า URI](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="4fe35-131">ตั้งค่า Key Vault สำหรับจัดเก็บ URI ของบัญชีการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="4fe35-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="4fe35-132">เปิด Key Vault ที่คุณตั้งใจที่จะใช้กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4fe35-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="4fe35-133">ไปที่ **การตั้งค่า** \> **ความลับ** แล้วเลือก **สร้าง/นำเข้า** เพื่อสร้างความลับใหม่</span><span class="sxs-lookup"><span data-stu-id="4fe35-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="4fe35-134">บนหน้า **สร้างความลับ** ในฟิลด์ **ตัวเลือกการอัพโหลด** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="4fe35-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="4fe35-135">ป้อนชื่อของความลับ</span><span class="sxs-lookup"><span data-stu-id="4fe35-135">Enter the name of the secret.</span></span> <span data-ttu-id="4fe35-136">ชื่อนี้จะใช้ในระหว่างการตั้งค่าบริการใน Regulatory Configuration Service (RCS) และจะถูกอ้างอิงถึง *ชื่อความลับของ Key Vault*</span><span class="sxs-lookup"><span data-stu-id="4fe35-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="4fe35-137">ในฟิลด์ **ค่า** ให้เลือก **URI ลายเซ็นที่ใช้การเข้าถึงร่วมกัน** แล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="4fe35-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="4fe35-138">ตั้งค่านโยบายการเข้าถึงเพื่อให้การออกใบแจ้งหนี้อิเล็กทรอนิกส์มีระดับที่ถูกต้องของการเข้าถึงที่ปลอดภัยไปยังข้อมูลลับที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4fe35-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="4fe35-139">ไปที่ **การตั้งค่า \> นโยบายการเข้าถึง** และเลือก **เพิ่มนโยบายการเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="4fe35-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="4fe35-140">ตั้งค่าสิทธิ์ลับ สำหรับการดำเนินงาน **รับ** และ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="4fe35-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![การให้สิทธิการเข้าถึงบริการ](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="4fe35-142">ตั้งค่าสิทธิ์ใบรับรอบ สำหรับการดำเนินงาน **รับ** และ **รายการ**</span><span class="sxs-lookup"><span data-stu-id="4fe35-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![การให้สิทธิ์ใบรับรอง](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="4fe35-144">ในเขตข้อมูล **เลือกเงินต้น** ให้เลือก **ไม่ได้เลือก**</span><span class="sxs-lookup"><span data-stu-id="4fe35-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="4fe35-145">ในกล่องโต้ตอบ **เงินต้น** ให้เลือกเงินต้นโดยการเพิ่ม **บริการใบแจ้งหนี้อิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="4fe35-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="4fe35-146">เลือก **เพิ่ม** แล้วเลือก **บันทึกการเปลี่ยนแปลง Key Vault**</span><span class="sxs-lookup"><span data-stu-id="4fe35-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="4fe35-147">บนหน้า **ภาพรวม** สำเนาค่า **ชื่อ DNS** สำหรับ Key Vault</span><span class="sxs-lookup"><span data-stu-id="4fe35-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="4fe35-148">ค่านี้จะใช้ในระหว่างการตั้งค่าของบริการใน RCS และจะถูกอ้างอิงเป็น *URI ของ Key Vault*</span><span class="sxs-lookup"><span data-stu-id="4fe35-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]