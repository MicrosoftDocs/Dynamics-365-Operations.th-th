---
title: เริ่มต้นใช้งานการบัญชีสินค้าคงคลังส่วนกลาง
description: หัวข้อนี้อธิบายวิธีการเริ่มต้นใช้งานการบัญชีสินค้าคงคลังส่วนกลาง
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301709"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="256c9-103">เริ่มต้นใช้งานการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="256c9-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="256c9-104">การบัญชีสินค้าคงคลังส่วนกลางช่วยให้คุณสามารถทำการบัญชีสินค้าคงคลังหลายรายการในบัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลางที่คุณตั้งค่าไว้</span><span class="sxs-lookup"><span data-stu-id="256c9-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="256c9-105">คุณต้องเชื่อมโยงแต่ละบัญชีแยกประเภทการบัญชีสินค้าคงคลังส่วนกลางกับ *แบบแผน*</span><span class="sxs-lookup"><span data-stu-id="256c9-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="256c9-106">แบบแผนเป็นชุดของนโยบายการบัญชีชนิดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="256c9-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="256c9-107">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="256c9-107">Cost object</span></span>
- <span data-ttu-id="256c9-108">เกณฑ์การวัดข้อมูลที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="256c9-108">Input measurement basis</span></span>
- <span data-ttu-id="256c9-109">สมมติฐานกระแสต้นทุน</span><span class="sxs-lookup"><span data-stu-id="256c9-109">Cost flow assumption</span></span>
- <span data-ttu-id="256c9-110">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="256c9-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="256c9-111">แม้แต่หลังจากที่คุณได้เปิดใช้งานการบัญชีสินค้าคงคลังส่วนกลางแล้ว คุณยังสามารถทำการบัญชีสินค้าคงคลังใน Microsoft Dynamics 365 Supply Chain Management ได้ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="256c9-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="256c9-112">การบัญชีสินค้าคงคลังส่วนกลางเป็น add-in</span><span class="sxs-lookup"><span data-stu-id="256c9-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="256c9-113">เมื่อต้องการทำให้คุณลักษณะพร้อมใช้งาน คุณต้องติดตั้งจาก Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="256c9-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="256c9-114">คุณจึงสามารถเลือกที่จะประเมินในสภาพแวดล้อมการทดสอบ ก่อนที่คุณจะเปิดใช้งานสำหรับสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="256c9-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="256c9-115">การบัญชีสินค้าคงคลังส่วนกลางไม่สนับสนุนลักษณะการงานการจัดการต้นทุนทั้งหมดที่สร้างไว้ใน Supply Chain Management ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="256c9-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="256c9-116">ดังนั้น จึงเป็นเรื่องสำคัญอย่างยิ่งที่คุณจะต้องประเมินว่าชุดของคุณลักษณะที่พร้อมใช้งานในขณะนี้จะตรงกับความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="256c9-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="256c9-117">วิธีการดูตัวอย่างสาธารณะการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="256c9-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="256c9-118">เมื่อต้องการใช้การบัญชีสินค้าคงคลังส่วนกลาง คุณต้องมีสภาพแวดล้อมความพร้อมใช้งานสูงที่เปิดใช้งาน LCS (ไม่ใช่สภาพแวดล้อม OneBox)</span><span class="sxs-lookup"><span data-stu-id="256c9-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="256c9-119">นอกจากนี้ คุณต้องรัน Supply Chain Management รุ่น 10.0.19 หรือใหม่กว่าด้วย</span><span class="sxs-lookup"><span data-stu-id="256c9-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="256c9-120">เมื่อต้องการลงทะเบียนตัวอย่างสาธารณะการบัญชีสินค้าคงคลังส่วนกลาง ให้ส่งรหัสสภาพแวดล้อม LCS ของคุณทางอีเมลไปยัง [ทีมงานการบัญชีสินค้าคงคลังส่วนกลาง](mailto:GlobalInventoryAccounting@service.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="256c9-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="256c9-121">หลังจากที่คุณได้รับอนุมัติใช้โปรแกรมแล้ว ทีมงานจะส่งอีเมลติดตามผลที่มีคีย์รุ่นเบต้าของการบัญชีสินค้าคงคลังส่วนกลางและตำแหน่งข้อมูลบริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="256c9-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="256c9-122">หลังจากที่คุณได้รับคีย์รุ่นเบต้า คุณสามารถ [ติดตั้ง Add-in](#install)</span><span class="sxs-lookup"><span data-stu-id="256c9-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="256c9-123">การให้ลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="256c9-123">Licensing</span></span>

<span data-ttu-id="256c9-124">การบัญชีสินค้าคงคลังส่วนกลางจะได้รับอนุญาตพร้อมกับคุณลักษณะมาตรฐานของการบัญชีสินค้าคงคลังที่พร้อมใช้งานสำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="256c9-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="256c9-125">คุณไม่จำเป็นต้องซื้อสิทธิ์การใช้งานเพิ่มเติมเพื่อใช้การบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="256c9-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="256c9-126">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="256c9-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="256c9-127">ตั้งค่าการรวม Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="256c9-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="256c9-128">ก่อนที่คุณจะสามารถเปิดใช้งานฟังก์ชัน Add-in คุณต้องรวม Microsoft Power Platform โดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="256c9-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="256c9-129">เปิดสภาพแวดล้อม LCS ที่คุณต้องการเพิ่มบริการ</span><span class="sxs-lookup"><span data-stu-id="256c9-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="256c9-130">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="256c9-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="256c9-131">ในส่วน **การรวม Power Platform** เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="256c9-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="256c9-132">ในกล่องโต้ตอบ **การตั้งค่าสภาพแวดล้อม Power Platform** ให้เลือกกล่องกาเครื่องหมาย แล้วเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="256c9-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="256c9-133">โดยทั่วไป การตั้งค่าจะจะใช้เวลาระหว่าง 60 และ 90 นาที</span><span class="sxs-lookup"><span data-stu-id="256c9-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="256c9-134">หลังจากการตั้งค่า สภาพแวดล้อม Microsoft Power Platform เสร็จสมบูรณ์แล้ว หน้าจะแสดงชื่อของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="256c9-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="256c9-135">นอกจากนี้ ส่วน **การรวม Power Platform** จะแสดงรายงาน "การตั้งค่าสภาพแวดล้อม Power Platform เสร็จสมบูรณ์แล้ว"</span><span class="sxs-lookup"><span data-stu-id="256c9-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="256c9-136">การบัญชีสินค้าคงคลังส่วนกลางไม่ต้องการแอปพลิเคชันการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="256c9-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="256c9-137">สำหรับข้อมูลเพิ่มเติม ให้ดู [ตั้งค่าหลังจากการปรับใช้สภาพแวดล้อม](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment)</span><span class="sxs-lookup"><span data-stu-id="256c9-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="256c9-138">ตั้งค่า Dataverse</span><span class="sxs-lookup"><span data-stu-id="256c9-138">Set up Dataverse</span></span>

<span data-ttu-id="256c9-139">ก่อนที่คุณจะตั้งค่า Dataverse เพิ่มหลักการบริการการบัญชีสินค้าคงคลังส่วนกลางให้กับผู้เช่าของคุณโดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="256c9-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="256c9-140">ติดตั้ง Azure AD Module สำหรับ Windows PowerShell v2 ตามที่อธิบายไว้ใน [ติดตั้ง Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2)</span><span class="sxs-lookup"><span data-stu-id="256c9-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="256c9-141">โดยรันคำสั่ง PowerShell ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="256c9-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="256c9-142">จากนั้น ให้สร้างผู้ใช้แอปพลิเคชันให้กับการบัญชีสินค้าคงคลังส่วนกลางใน Dataverse โดยปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="256c9-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="256c9-143">เปิด URL ของสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="256c9-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="256c9-144">ไปที่ **การตั้งค่าขั้นสูง \> ระบบ \> ความปลอดภัย \> ผู้ใช้** และสร้างผู้ใช้แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="256c9-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="256c9-145">ใช้ฟิลด์ **มุมมอง** เพื่อเปลี่ยนมุมมองหน้าเป็น *ผู้ใช้แอปพลิเคชัน*</span><span class="sxs-lookup"><span data-stu-id="256c9-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="256c9-146">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="256c9-146">Select **New**.</span></span>
1. <span data-ttu-id="256c9-147">ตั้งค่าฟิลด์ **รหัสแอพลิเคชัน** เป็น *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*</span><span class="sxs-lookup"><span data-stu-id="256c9-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="256c9-148">เลือก **กําหนดบทบาท** แล้วเลือก *ผู้ดูแลระบบ*</span><span class="sxs-lookup"><span data-stu-id="256c9-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="256c9-149">ถ้ามีบทบาทที่มีชื่อ *ผู้ใช้ Common Data Service* ให้เลือกบทบาทนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="256c9-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="256c9-150">ทําซ้ําขั้นตอนก่อนหน้านี้ แต่ตั้งค่าฟิลด์ **รหัสแอปพลิเคชัน** เป็น *5f58fc56-0202-49a8-ac9e-0946b049718b*</span><span class="sxs-lookup"><span data-stu-id="256c9-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="256c9-151">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผู้ใช้แอพลิเคชัน](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)</span><span class="sxs-lookup"><span data-stu-id="256c9-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="256c9-152">ถ้าภาษาเริ่มต้นของการติดตั้ง Dataverse ของคุณไม่ใช่ภาษาอังกฤษ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="256c9-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="256c9-153">ไปที่ **การตั้งค่าขั้นสูง \> การจัดการ \> ภาษา**</span><span class="sxs-lookup"><span data-stu-id="256c9-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="256c9-154">เลือก *ภาษาอังกฤษ* (*LanguageCode=1033*) และจากนั้นเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="256c9-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="256c9-155">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="256c9-155">Install the add-in</span></span>

<span data-ttu-id="256c9-156">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อติดตั้ง Add-in เพื่อให้คุณสามารถใช้การลงบัญชีสินค้าคงคลังส่วนกลางได้</span><span class="sxs-lookup"><span data-stu-id="256c9-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="256c9-157">[ลงทะเบียน](#sign-up) สำหรับวิธีการดูตัวอย่างสาธารณะการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="256c9-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="256c9-158">ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com/Logon/Index)</span><span class="sxs-lookup"><span data-stu-id="256c9-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="256c9-159">ไปที่ **การจัดการคุณลักษณะการแสดงตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="256c9-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="256c9-160">เลือกเครื่องหมายบวก (**+**)</span><span class="sxs-lookup"><span data-stu-id="256c9-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="256c9-161">ในฟิลด์ **รหัส** ให้ป้อนคีย์เบต้า add-in ของคุณสำหรับการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="256c9-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="256c9-162">(คุณควรได้รับคีย์รุ่นเบต้าของคุณทางอีเมลเมื่อคุณลงชื่อสมัคร)</span><span class="sxs-lookup"><span data-stu-id="256c9-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="256c9-163">เลือก **ยกเลิกการบล็อก**</span><span class="sxs-lookup"><span data-stu-id="256c9-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="256c9-164">เปิดสภาพแวดล้อม LCS ที่คุณต้องการเพิ่มบริการ</span><span class="sxs-lookup"><span data-stu-id="256c9-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="256c9-165">ไปที่ **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="256c9-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="256c9-166">ไปที่ **การรวม Power Platform** และเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="256c9-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="256c9-167">ในกล่องโต้ตอบ **การตั้งค่าสภาพแวดล้อม Power Platform** ให้เลือกกล่องกาเครื่องหมาย แล้วเลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="256c9-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="256c9-168">โดยทั่วไป การตั้งค่าจะจะใช้เวลาระหว่าง 60 และ 90 นาที</span><span class="sxs-lookup"><span data-stu-id="256c9-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="256c9-169">หลังจากการตั้งค่าสภาพแวดล้อม Microsoft Power Platform เสร็จสมบูรณ์แล้ว บนแท็บด่วน **Add-in ของสภาพแวดล้อม** ให้เลือก **ติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="256c9-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="256c9-170">เลือก **การบัญชีสินค้าคงคลังส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="256c9-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="256c9-171">ปฏิบัติตามคำแนะนำการติดตั้ง และยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="256c9-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="256c9-172">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="256c9-172">Select **Install**.</span></span>
1. <span data-ttu-id="256c9-173">บน FastTab **Add-in ของสภาพแวดล้อม** คุณควรเห็นว่ามีการติดตั้งการบัญชีสินค้าคงคลังส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="256c9-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="256c9-174">หลังจากสองสามนาที สถานะควรเปลี่ยนจาก *กำลังติดตั้ง* เป็น *ติดตั้งแล้ว*</span><span class="sxs-lookup"><span data-stu-id="256c9-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="256c9-175">(คุณอาจต้องรีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงนี้) ณ จุดนั้น การบัญชีสินค้าคงคลังส่วนกลางจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="256c9-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="256c9-176">ตั้งค่าการรวม</span><span class="sxs-lookup"><span data-stu-id="256c9-176">Set up the integration</span></span>

<span data-ttu-id="256c9-177">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าการรวมระหว่างการบัญชีสินค้าคงคลังส่วนกลางและ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="256c9-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="256c9-178">ลงชื่อเข้าใช้ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="256c9-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="256c9-179">ไปที่ **การจัดการระบบ \> การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="256c9-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="256c9-180">เลือก **ตรวจหาการอัพเดต**</span><span class="sxs-lookup"><span data-stu-id="256c9-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="256c9-181">บนแท็บ **ทั้งหมด** ให้ค้นหาลักษณะการงานที่มีชื่อว่า *การบัญชีสินค้าคงคลังส่วนกลาง*</span><span class="sxs-lookup"><span data-stu-id="256c9-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="256c9-182">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="256c9-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="256c9-183">ไปที่ **การบัญชีสินค้าคงคลังส่วนกลาง \> การตั้งค่า \> พารามิเตอร์การบัญชีสินค้าคงคลังส่วนกลาง \> พารามิเตอร์การรวม**</span><span class="sxs-lookup"><span data-stu-id="256c9-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="256c9-184">ในฟิลด์ **ปลายทางของบริการข้อมูล** และ **ปลายทางการบัญชีสินค้าคงคลังส่วนกลาง** ให้ป้อน URL จากอีเมลที่ส่งทีมการบัญชีสินค้าคงคลังส่วนกลางเมื่อคุณลงชื่อสมัครดูตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="256c9-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="256c9-185">ขณะนี้ การบัญชีสินค้าคงคลังส่วนกลางพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="256c9-185">Global Inventory Accounting is now ready to use.</span></span>
