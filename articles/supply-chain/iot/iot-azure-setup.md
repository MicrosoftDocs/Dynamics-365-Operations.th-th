---
title: ตั้งค่าทรัพยากร Azure สำหรับเครื่องมือ IoT
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างและตั้งค่าคอนฟิกทรัพยากร Microsoft Azure ที่จำเป็นสำหรับเครื่องมือ IoT
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cd06410dd6260e6a371b0044546be7f8c9957c80
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989832"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="6bf5a-103">ตั้งค่าทรัพยากร Azure สำหรับเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6bf5a-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างและตั้งค่าคอนฟิกทรัพยากร Microsoft Azure ที่จำเป็นสำหรับเครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="6bf5a-105">สร้างแหล่งข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="6bf5a-105">Create Azure resources</span></span>

<span data-ttu-id="6bf5a-106">ทำตามขั้นตอนต่อไปนี้เพื่อสร้างฮับ IoT แคช Redis และ Key Vault ที่สามารถเข้าถึงได้โดย Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6bf5a-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="6bf5a-107">ตรวจสอบว่ารหัสของแอปพลิเคชันของบุคคลที่หนึ่งของ Microsoft Dynamics ERP Microservices อยู่ในผู้เช่าของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6bf5a-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="6bf5a-108">เมื่อต้องการตรวจสอบว่ารหัสแอปพลิเคชันของแอปพลิเคชันของบุคคลที่หนึ่งของ Microsoft Dynamics ERP Microservices อยู่ในผู้เช่าของคุณ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-109">ล็อกอินไปยังพอร์ทัล Azure ที่ <https://portal.azure.com></span><span class="sxs-lookup"><span data-stu-id="6bf5a-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="6bf5a-110">ไปที่ **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="6bf5a-111">ไปที่ **แอปพลิเคชันองค์กร**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="6bf5a-112">ในฟิลด์ **ชนิดของแอปพลิเคชัน** เลือก **แอปพลิเคชัน Microsoft**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="6bf5a-113">ในฟิลด์การค้นหา ป้อน **Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="6bf5a-114">ตรวจสอบว่า **Microsoft Dynamics ERP Microservices** อยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="6bf5a-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="6bf5a-115">แอปพลิเคชันอื่นมีชื่อที่คล้ายกัน</span><span class="sxs-lookup"><span data-stu-id="6bf5a-115">Other applications have similar names.</span></span> <span data-ttu-id="6bf5a-116">ดังนั้น ควรตรวจสอบให้แน่ใจว่าคุณค้นหาแอปพลิเคชันที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6bf5a-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="6bf5a-117">รหัสของแอปพลิเคชันคือ **0cdb527f-a8d1-4bf8-9436-b352c68682b2**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="6bf5a-118">ถ้าแอปพลิเคชันไม่ได้อยู่ในรายการ คุณต้องเพิ่มไปยังผู้เช่าของคุณ:</span><span class="sxs-lookup"><span data-stu-id="6bf5a-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="6bf5a-119">ในพอร์ทัล Azure บนแถบเครื่องมือ ให้เลือกปุ่มเพื่อเปิด Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="6bf5a-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="6bf5a-120">รันคำสั่ง **Install-Module AzureAD**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="6bf5a-121">ป้อน **Y** เพื่อติดตั้งโมดูล</span><span class="sxs-lookup"><span data-stu-id="6bf5a-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="6bf5a-122">รันคำสั่ง **Get-InstalledModule -Name "AzureAD"** เพื่อตรวจสอบว่ามีการติดตั้งโมดูล</span><span class="sxs-lookup"><span data-stu-id="6bf5a-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="6bf5a-123">รันคำสั่ง **Connect-AzureAD -Confirm** เพื่อรันการตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="6bf5a-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="6bf5a-124">รันคำสั่ง **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="6bf5a-125">ขณะนี้คุณสามารถทำซ้ำขั้นตอนที่1 ถึง 6 เพื่อตรวจสอบว่ารหัสของแอปอยู่ในผู้เช่าของคุณหรือไม่</span><span class="sxs-lookup"><span data-stu-id="6bf5a-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="6bf5a-126">สร้างทรัพยากร Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bf5a-126">Create a key vault resource</span></span>

<span data-ttu-id="6bf5a-127">เมื่อต้องการสร้างทรัพยากร Key Vault ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-128">ในพอร์ทัล Azure สร้างหรือไปที่กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6bf5a-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="6bf5a-129">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-129">Select **Add**.</span></span>
3. <span data-ttu-id="6bf5a-130">บนหน้า **สร้าง** ในฟิลด์การค้นหา ให้ป้อน **Key Vault**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="6bf5a-131">จากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-131">Then select **Create**.</span></span>
4. <span data-ttu-id="6bf5a-132">บนหน้า **สร้าง Key vault** ในฟิลด์ **ชื่อของ Key Vault** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="6bf5a-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="6bf5a-133">ตรวจทานค่าเริ่มต้นแล้วเลือก **ตรวจทาน + สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="6bf5a-134">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-134">Select **Create**.</span></span>

<span data-ttu-id="6bf5a-135">มีการสร้าง Key Vault ไว้ในพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="6bf5a-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="6bf5a-136">สร้างทรัพยากรฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-136">Create an IoT hub resource</span></span>

<span data-ttu-id="6bf5a-137">เมื่อต้องการสร้างทรัพยากรฮับ IoT ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-138">สร้างหรือไปที่กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6bf5a-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="6bf5a-139">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-139">Select **Add**.</span></span>
3. <span data-ttu-id="6bf5a-140">บนหน้า **สร้าง** ในฟิลด์การค้นหา ให้ป้อน **ฮับ IoT**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="6bf5a-141">จากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-141">Then select **Create**.</span></span>
4. <span data-ttu-id="6bf5a-142">ในฟิลด์ **ชื่อฮับ IoT** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="6bf5a-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="6bf5a-143">ตรวจทานค่าเริ่มต้นแล้วเลือก **ตรวจทาน + สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="6bf5a-144">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-144">Select **Create**.</span></span>

<span data-ttu-id="6bf5a-145">มีการสร้างฮับ IoT ไว้ในพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="6bf5a-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="6bf5a-146">เราขอแนะนำให้คุณสร้างทรัพยากรฮับ IoT เดียวเท่านั้นสำหรับแต่ละสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="6bf5a-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="6bf5a-147">สร้างทรัพยากรแคช Redis</span><span class="sxs-lookup"><span data-stu-id="6bf5a-147">Create a Redis cache resource</span></span>

<span data-ttu-id="6bf5a-148">เมื่อต้องการสร้างทรัพยากรแคช Redis ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-149">สร้างหรือไปที่กลุ่มทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="6bf5a-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="6bf5a-150">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-150">Select **Add**.</span></span>
3. <span data-ttu-id="6bf5a-151">บนหน้า **สร้าง** ในฟิลด์การค้นหา ให้ป้อน **แคช Azure สำหรับ Redis**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="6bf5a-152">จากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-152">Then select **Create**.</span></span>
4. <span data-ttu-id="6bf5a-153">ในฟิลด์ **ชื่อ DNS** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="6bf5a-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="6bf5a-154">ตรวจทานค่าเริ่มต้นแล้วเลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="6bf5a-155">มีการสร้างแคช Redis ไว้ในพื้นหลัง</span><span class="sxs-lookup"><span data-stu-id="6bf5a-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="6bf5a-156">เราขอแนะนำให้คุณสร้างแคช Redis เดียวเท่านั้นสำหรับแต่ละสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="6bf5a-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="6bf5a-157">ขณะนี้มีการสร้างทรัพยากรทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="6bf5a-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="6bf5a-158">ตั้งค่าคอนฟิกทรัพยากร Azure</span><span class="sxs-lookup"><span data-stu-id="6bf5a-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="6bf5a-159">ตั้งค่าคอนฟิกฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-159">Configure the IoT hub</span></span>

<span data-ttu-id="6bf5a-160">หากต้องการตั้งค่าคอนฟิกฮับ IoT ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-161">ในทรัพยากรของคุณ ให้เลือกทรัพยากรฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="6bf5a-162">ในบานหน้าต่างนำทางด้านซ้ายให้เลือก **ปลายทางที่มีอยู่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="6bf5a-163">ภายใต้ **กลุ่มผู้บริโภค** ให้วางกลุ่มผู้บริโภคต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="6bf5a-164">กลุ่มผู้บริโภคเหล่านี้จะสอดคล้องกับสถานการณ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="6bf5a-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="6bf5a-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="6bf5a-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="6bf5a-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="6bf5a-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="6bf5a-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="6bf5a-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="6bf5a-168">ตั้งค่าคอนฟิก Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bf5a-168">Configure the key vault</span></span>

<span data-ttu-id="6bf5a-169">หากต้องการตั้งค่าคอนฟิก Key Vault ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-170">ในทรัพยากรของคุณ ให้เลือกทรัพยากร Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bf5a-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="6bf5a-171">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **นโยบายการเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="6bf5a-172">เลือก **เพิ่มนโยบายการเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="6bf5a-173">บนหน้า **เพิ่มนโยบายการเข้าถึง** ในฟิลด์ **สิทธิ์ลับ** เลือก **รับ** และ **แสดงรายการ**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="6bf5a-174">คลิกใน **หลักการเลือก**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="6bf5a-175">ในกล่องโต้ตอบ **หลัก** ให้ค้นหาและเลือก **Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="6bf5a-176">แล้วเลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-176">Then select **Select**.</span></span>
7. <span data-ttu-id="6bf5a-177">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-177">Select **Add**.</span></span>
8. <span data-ttu-id="6bf5a-178">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-178">Select **Save**.</span></span>

<span data-ttu-id="6bf5a-179">ขณะนี้แอปพลิเคชันมีสิทธิ์เข้าถึงข้อมูลลับใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bf5a-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="6bf5a-180">บันทึกข้อมูลลับของสตริงการเชื่อมต่อฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="6bf5a-181">เมื่อต้องการบันทึกข้อมูลลับสำหรับสตริงการเชื่อมต่อฮับ IoT ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-182">ในทรัพยากรของคุณ ให้เลือกทรัพยากรฮับ IoT</span><span class="sxs-lookup"><span data-stu-id="6bf5a-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="6bf5a-183">ในบานหน้าต่างนำทางด้านซ้ายให้เลือก **ปลายทางที่มีอยู่แล้ว**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="6bf5a-184">คัดลอกค่าในฟิลด์ **ปลายทางฮับเหตุการณ์ที่เข้ากันได้**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="6bf5a-185">ไปที่ทรัพยากร Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bf5a-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="6bf5a-186">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="6bf5a-187">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="6bf5a-188">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="6bf5a-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="6bf5a-189">ในฟิลด์ **ค่า** ให้วางค่าปลายทางที่คุณคัดลอกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="6bf5a-190">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="6bf5a-191">บันทึกข้อมูลลับของสตริงการเชื่อมต่อแคช Redis</span><span class="sxs-lookup"><span data-stu-id="6bf5a-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="6bf5a-192">เมื่อต้องการบันทึกข้อมูลลับสำหรับสตริงการเชื่อมต่อแคช Redis ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="6bf5a-193">ในทรัพยากรของคุณ ให้เลือกทรัพยากรแคช Redis</span><span class="sxs-lookup"><span data-stu-id="6bf5a-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="6bf5a-194">เลือก **คีย์การเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="6bf5a-195">การคัดลอกค่าในฟิลด์ **สตริงการเชื่อมต่อหลัก**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="6bf5a-196">ไปที่ทรัพยากร Key Vault</span><span class="sxs-lookup"><span data-stu-id="6bf5a-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="6bf5a-197">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="6bf5a-198">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="6bf5a-199">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="6bf5a-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="6bf5a-200">ในฟิลด์ **ค่า** ให้วางสตริงการเชื่อมต่อที่คุณคัดลอกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6bf5a-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="6bf5a-201">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="6bf5a-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="6bf5a-202">เมื่อใดก็ตามที่คุณอัปเดตสตริงการเชื่อมต่ออใดๆ คุณต้องอัปเดตค่าข้อมูลลับเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="6bf5a-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="6bf5a-203">ขณะนี้คุณได้เสร็จสิ้นการเตรียมใช้งานทรัพยากร Azure ที่จำเป็นแล้ว</span><span class="sxs-lookup"><span data-stu-id="6bf5a-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="6bf5a-204">ขั้นตอนต่อไปคือการ [ติดตั้ง Add-in เครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md)</span><span class="sxs-lookup"><span data-stu-id="6bf5a-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
