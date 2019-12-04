---
title: ติดตั้งและกำหนดค่าภาพรวมแอปคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการติดตั้งและกำหนดค่า Dynamics 365 for Finance and Operations
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: df0bc9ff2405cc2f370ea777a70e005a1ff338a0
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814961"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a><span data-ttu-id="5b808-103">ติดตั้งและกำหนดค่าภาพรวมแอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b808-103">Install and configure the Warehousing app overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> <span data-ttu-id="5b808-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกคลังสินค้าสำหรับการปรับใช้ cloud</span><span class="sxs-lookup"><span data-stu-id="5b808-104">This topic describes how to configure warehousing for cloud deployments.</span></span> <span data-ttu-id="5b808-105">ถ้าคุณกำลังค้นหาวิธีการตั้งค่าคอนฟิกคลังสินค้าสำหรับการปรับใช้ในองค์กร โปรดดู [คลังสินค้าสำหรับการปรับใช้ในองค์กร](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md)</span><span class="sxs-lookup"><span data-stu-id="5b808-105">If you are looking for how to configure warehousing for on-premises deployments, please see [Warehousing for on-premises deployments](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).</span></span>


<span data-ttu-id="5b808-106">หัวข้อนี้อธิบายวิธีการติดตั้งและกำหนดค่า Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b808-106">This topic describes how to install and configure Dynamics 365 for Finance and Operations – Warehousing app.</span></span>

<span data-ttu-id="5b808-107">แอปคลังสินค้ามีอยู่ใน Google Play Store และ Windows Store</span><span class="sxs-lookup"><span data-stu-id="5b808-107">Warehousing app is available on Google Play Store and Windows Store.</span></span> <span data-ttu-id="5b808-108">สำหรับ Dynamics 365 Supply Chain Management รุ่นปัจจุบัน แอพลิเคชันนี้มีไว้สำหรับเป็นส่วนประกอบแบบสแตนด์อโลน ซึ่งหมายถึงการปรับใช้ด้วยตนเองบนอุปกรณ์ที่ใช้สำหรับงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b808-108">For the current version of Dynamics 365 Supply Chain Management, this app is provided as a standalone component, which means self-deployment on devices used for warehouse tasks.</span></span> <span data-ttu-id="5b808-109">เมื่อต้องการใช้แอพลิเคชัน คุณต้องดาวน์โหลดแอปบนอุปกรณ์แต่ละเครื่องและตั้งค่าคอนฟิกเพื่อเชื่อมต่อกับสภาพแวดล้อมของ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b808-109">In order to use the app, you must download the app on each device and configure it to connect to your Supply Chain Management environment.</span></span> <span data-ttu-id="5b808-110">หัวข้อนี้อธิบายวิธีการติดตั้งแอพบนอุปกรณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b808-110">This topic describes how to install the app on your devices.</span></span> <span data-ttu-id="5b808-111">นอกจากนี้ยังอธิบายถึงวิธีการตั้งค่าคอนฟิกแอพเพื่อเชื่อมต่อกับสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5b808-111">It also explains how to configure the app to connect to your Supply Chain Management environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b808-112">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="5b808-112">Prerequisites</span></span>
<span data-ttu-id="5b808-113">แอปพร้อมใช้งานในระบบปฏิบัติการ Android และ Windows</span><span class="sxs-lookup"><span data-stu-id="5b808-113">The app is available on Android and Windows operating systems.</span></span> <span data-ttu-id="5b808-114">เมื่อต้องการใช้แอพนี้ คุณต้องใช้ระบบปฏิบัติการที่ได้รับการสนับสนุนต่อไปนี้ที่ติดตั้งบนอุปกรณ์ของคุณอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="5b808-114">To use this app, you must have one of the following supported operating systems installed on your devices.</span></span> <span data-ttu-id="5b808-115">คุณต้องมีหนึ่งในรุ่นที่รองรับต่อไปนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="5b808-115">You must also have one of the following supported versions.</span></span> <span data-ttu-id="5b808-116">ใช้ข้อมูลในตารางต่อไปนี้ในการประเมินว่าสภาพแวดล้อมของฮาร์ดแวร์และซอฟต์แวร์ของคุณพร้อมที่จะสนับสนุนการติดตั้งหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5b808-116">Use the information in the following table to evaluate if your hardware and software environment is ready to support the installation.</span></span>

| <span data-ttu-id="5b808-117">แพลตฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="5b808-117">Platform</span></span>                    | <span data-ttu-id="5b808-118">รุ่น</span><span class="sxs-lookup"><span data-stu-id="5b808-118">Version</span></span>                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b808-119">Android</span><span class="sxs-lookup"><span data-stu-id="5b808-119">Android</span></span>                     | <span data-ttu-id="5b808-120">4.4, 5.0, 6.0, 7.0, 8.0, 9.0</span><span class="sxs-lookup"><span data-stu-id="5b808-120">4.4, 5.0, 6.0, 7.0, 8.0, 9.0</span></span>                                                                                                                                                     |
| <span data-ttu-id="5b808-121">% 1 </span><span class="sxs-lookup"><span data-stu-id="5b808-121">Windows (UWP)</span></span>               | <span data-ttu-id="5b808-122">Windows 10 (ทุกรุ่น)</span><span class="sxs-lookup"><span data-stu-id="5b808-122">Windows 10 (all versions)</span></span>                                                                                                                                                   |
| <span data-ttu-id="5b808-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b808-123">Finance and Operations</span></span> | <span data-ttu-id="5b808-124">Microsoft Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="5b808-124">Microsoft Dynamics 365 for Operations, version 1611</span></span> <br><span data-ttu-id="5b808-125">หรือ</span><span class="sxs-lookup"><span data-stu-id="5b808-125">-or-</span></span> <br><span data-ttu-id="5b808-126">Microsoft Dynamics AX รุ่น 7.0/7.0.1 และ Microsoft Dynamics AX การปรับปรุงแพลตฟอร์ม 2 พร้อมกับโปรแกรมแก้ไขด่วน KB 3210014</span><span class="sxs-lookup"><span data-stu-id="5b808-126">Microsoft Dynamics AX version 7.0/7.0.1 and Microsoft Dynamics AX platform update 2 with hotfix KB 3210014</span></span> |

## <a name="get-the-app"></a><span data-ttu-id="5b808-127">เรียกกลุ่มแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="5b808-127">Get the app</span></span>
-   <span data-ttu-id="5b808-128">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="5b808-128">Windows (UWP)</span></span>
     - [<span data-ttu-id="5b808-129">Finance and Operations - คลังสินค้าบน Windows Store</span><span class="sxs-lookup"><span data-stu-id="5b808-129">Finance and Operations - Warehousing on the Windows Store</span></span>](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   <span data-ttu-id="5b808-130">Android</span><span class="sxs-lookup"><span data-stu-id="5b808-130">Android</span></span>
    - [<span data-ttu-id="5b808-131">Finance and Operations - คลังสินค้าบน Google Play Store</span><span class="sxs-lookup"><span data-stu-id="5b808-131">Finance and Operations - Warehousing on the Google Play Store</span></span>](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> <span data-ttu-id="5b808-132">แกลเลอรีแอป Zebra ได้ถูกเลิกใช้ ซึ่งหมายความว่าแอป Warehousing จะไม่พร้อมใช้งานอีกต่อไปสำหรับการดาวน์โหลดจากสถานที่นั้น</span><span class="sxs-lookup"><span data-stu-id="5b808-132">The Zebra App Gallery has been retired, which means that the Warehousing app will no longer be available for download from that location.</span></span>

## <a name="create-a-web-service-application-in-azure-active-directory"></a><span data-ttu-id="5b808-133">สร้างแอพลิเคชัน Web Service ใน Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b808-133">Create a web service application in Azure Active Directory</span></span>
<span data-ttu-id="5b808-134">เพื่อเปิดใช้งานแอปให้ทำงานกับเซิร์ฟเวอร์ Supply Chain Management เฉพาะ คุณต้องลงทะเบียนแอพลิเคชัน Web Service ในผู้เช่า Azure Active Directory สำหรับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b808-134">To enable the app to interact with a specific Supply Chain Management server, you must register a web service application in an Azure Active Directory for the Supply Chain Management tenant.</span></span> <span data-ttu-id="5b808-135">สำหรับเหตุผลด้านความปลอดภัย เราขอแนะนำให้คุณสร้างแอพบริการเว็บสำหรับแต่ละอุปกรณ์ที่คุณใช้</span><span class="sxs-lookup"><span data-stu-id="5b808-135">For security reasons, we recommend that you create a web service application for each device that you use.</span></span> <span data-ttu-id="5b808-136">เพื่อสร้างแอพลิเคชัน Web Service ใน Azure Active Directory (Azure AD) ให้ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="5b808-136">To create a web service application in Azure Active Directory (Azure AD), complete the following steps:</span></span>

1.  <span data-ttu-id="5b808-137">ในเว็บเบราเซอร์ ไปที่ <https://portal.azure.com></span><span class="sxs-lookup"><span data-stu-id="5b808-137">In a web browser, go to <https://portal.azure.com>.</span></span>
2.  <span data-ttu-id="5b808-138">ป้อนชื่อและรหัสผ่านสำหรับผู้ใช้ที่มีสิทธิ์เข้าถึงการสมัครใช้งาน Azure</span><span class="sxs-lookup"><span data-stu-id="5b808-138">Enter the name and password for the user who has access to the Azure subscription.</span></span>
3.  <span data-ttu-id="5b808-139">ในพอร์ทัล Azure ในบานหน้าต่างนำทางด้านซ้าย ให้คลิก **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="5b808-139">In Azure Portal, in the left navigation pane, click **Azure Active Directory**.</span></span>

    <span data-ttu-id="5b808-140">[![WMA-01-ใช้งาน-ไดเรกทอรี-ตัวอย่าง](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-140">[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)</span></span>

4.  <span data-ttu-id="5b808-141">ตรวจสอบว่าอินสแตนซ์ของ Active Directory เป็นรายการที่ถูกใช้โดย Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b808-141">Ensure that the Active Directory instance is the one that is used by Supply Chain Management.</span></span>
5.  <span data-ttu-id="5b808-142">ในรายการ คลิก **การลงทะเบียนแอพ**</span><span class="sxs-lookup"><span data-stu-id="5b808-142">In the list, click **App registrations**.</span></span> 

    <span data-ttu-id="5b808-143">[![WMA-02-ใช้งาน-ไดเรกทอรี-แอพ-การลงทะเบียน](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-143">[![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)</span></span>

6.  <span data-ttu-id="5b808-144">ในบานหน้าต่างด้านบนสุด คลิก **การลงทะเบียนใหม่**</span><span class="sxs-lookup"><span data-stu-id="5b808-144">In the top pane, click **New registration**.</span></span> <span data-ttu-id="5b808-145">ตัวช่วยสร้าง **ลงทะเบียนแอพลิเคชัน** เริ่มทำงาน</span><span class="sxs-lookup"><span data-stu-id="5b808-145">The **Register an application wizard** starts.</span></span>
7.  <span data-ttu-id="5b808-146">ป้อนชื่อของแอพลิเคชันและ **เลือกบัญชีในไดเรกทอรี**ขององค์กรนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5b808-146">Enter a name for the application and select **Accounts in this organizational directory only**.</span></span> <span data-ttu-id="5b808-147">คลิก **ลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="5b808-147">Click **Register**.</span></span>  

    <span data-ttu-id="5b808-148">[![WMA-03-ใช้งาน-ไดเรกทอรี-เพิ่ม-แอพลิเคชัน](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-148">[![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)</span></span>

8.  <span data-ttu-id="5b808-149">การลงทะเบียนแอปใหม่ของคุณจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="5b808-149">Your new app registration will open.</span></span> 

    <span data-ttu-id="5b808-150">[![WMA-04-ใช้งาน-ไดเรกทอรี-ตั้งค่าคอนฟิก-แอพ](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-150">[![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)</span></span>

9.  <span data-ttu-id="5b808-151">อย่าลืม **รหัสแอพลิเคชัน** คุณจะต้องใช้ข้อมูลนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="5b808-151">Remember the **Application ID**, you will need it later.</span></span> <span data-ttu-id="5b808-152">ในภายหลัง **รหัสแอพลิเคชัน** จะถูกเรียกว่าเป็น **รหัสไคลเอนต์**</span><span class="sxs-lookup"><span data-stu-id="5b808-152">The **Application ID** will later be referred to as the **Client ID**.</span></span>
10. <span data-ttu-id="5b808-153">คลิก**ใบรับรอง** & ความ**ลับ**ในบานหน้าต่างจัดการ</span><span class="sxs-lookup"><span data-stu-id="5b808-153">Click **Certificate & secrets** in the **Manage** pane.</span></span> <span data-ttu-id="5b808-154">คลิกที่**ลับ**ใหม่ของไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="5b808-154">Click on **New client secret**.</span></span> 

    <span data-ttu-id="5b808-155">[![WMA-05-ใช้งาน-ไดเรกทอรี-สร้าง-คีย์](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-155">[![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)</span></span>

11. <span data-ttu-id="5b808-156">สร้างคีย์ โดยการป้อนคำอธิบายคีย์และระยะเวลาในส่วน **รหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="5b808-156">Create a key by entering a key description and a duration in the **Passwords** section.</span></span> <span data-ttu-id="5b808-157">คลิก **เพิ่ม** และคัดลอกคีย์</span><span class="sxs-lookup"><span data-stu-id="5b808-157">Click **Add** and copy the key.</span></span> <span data-ttu-id="5b808-158">ในภายหลังจะเรียกคีย์นี้ว่า **ข้อมูลลับไคลเอนต์**</span><span class="sxs-lookup"><span data-stu-id="5b808-158">This key will later be referred to as the **Client secret**.</span></span> 

    <span data-ttu-id="5b808-159">[![WMA-06-ใช้งาน-ไดเรกทอรี-บันทึก-คีย์](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-159">[![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)</span></span>

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><span data-ttu-id="5b808-160">สร้างและตั้งค่าคอนฟิกบัญชีผู้ใช้ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b808-160">Create and configure a user account in Supply Chain Management</span></span>
<span data-ttu-id="5b808-161">เพื่อเปิดใช้งาน Supply Chain Managementto เพื่อใช้แอพลิเคชัน Azure AD ของคุณ คุณต้องทำขั้นตอนการตั้งค่าคอนฟิกต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="5b808-161">To enable Supply Chain Managementto use your Azure AD application, you need to complete the following configuration steps:</span></span>

1.  <span data-ttu-id="5b808-162">สร้างผู้ใช้ที่สอดคล้องกับข้อมูลประจำตัวผู้ใช้แอพคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b808-162">Create a user that corresponds to the warehousing app user credentials.</span></span>
    1.  <span data-ttu-id="5b808-163">ไปที่ **การจัดการระบบ** &gt; **ทั่วไป** &gt; **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="5b808-163">Go to **System administration** &gt; **Common** &gt; **Users**.</span></span>
    2.  <span data-ttu-id="5b808-164">สร้างผู้ใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="5b808-164">Create a new user.</span></span>
    3.  <span data-ttu-id="5b808-165">กำหนดผู้ใช้อุปกรณ์เคลื่อนที่คลังสินค้าดังที่แสดงไว้ในภาพหน้าจอต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5b808-165">Assign the Warehouse mobile device user, as shown in the following screenshot.</span></span> 
    
        <span data-ttu-id="5b808-166">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-166">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span></span>

2.  <span data-ttu-id="5b808-167">เชื่อมโยงแอพลิเคชัน Azure Active Directory ของคุณกับผู้ใช้แอปคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b808-167">Associate your Azure Active Directory application with the warehousing app user.</span></span>
    1.  <span data-ttu-id="5b808-168">ใน Supply Chain Management ไปที่ **การดูแลระบบ** &gt; **การตั้งค่า** &gt; **แอพลิเคชัน Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="5b808-168">In Supply Chain Management, go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
    2.  <span data-ttu-id="5b808-169">สร้างบรรทัดใหม่ </span><span class="sxs-lookup"><span data-stu-id="5b808-169">Create a new line.</span></span>
    3.  <span data-ttu-id="5b808-170">ป้อน **รหัสไคลเอนต์** (ได้รับมาในส่วนสุดท้าย) ตั้งชื่อ และเลือกผู้ใช้ที่สร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5b808-170">Enter the **Client ID** (obtained in the last section), give it a name, and select the previously created user.</span></span> <span data-ttu-id="5b808-171">เราขอแนะนำให้คุณติดแท็กให้กับอุปกรณ์ทุกเครื่องของคุณเพื่อให้คุณสามารถลบสิทธิ์การเข้าถึง Supply Chain Management จากหน้านี้ได้อย่างง่ายดายในกรณีที่อุปกรณ์ของคุณหายไป</span><span class="sxs-lookup"><span data-stu-id="5b808-171">We recommend that you tag all your devices so that you can easily remove their access to Supply Chain Management from this page in case they are lost.</span></span> 
    
        <span data-ttu-id="5b808-172">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-172">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span></span>

## <a name="configure-the-application"></a><span data-ttu-id="5b808-173">ตั้งค่าคอนฟิกแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="5b808-173">Configure the application</span></span>
<span data-ttu-id="5b808-174">คุณต้องตั้งค่าคอนฟิกแอปบนอุปกรณ์เพื่อเชื่อมต่อในเซิร์ฟเวอร์ Supply Chain Management ผ่านทางแอพลิเคชัน Azure AD</span><span class="sxs-lookup"><span data-stu-id="5b808-174">You must configure the app on the device to connect to the Supply Chain Management server through the Azure AD application.</span></span> <span data-ttu-id="5b808-175">เมื่อต้องการทำเช่นนี้ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5b808-175">To do this, complete the following steps.</span></span>

1.  <span data-ttu-id="5b808-176">ในแอพ ไปที่ **การตั้งค่าการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="5b808-176">In the app, go to **Connection settings**.</span></span>
2.  <span data-ttu-id="5b808-177">ล้างฟิลด์ **โหมดสาธิต**</span><span class="sxs-lookup"><span data-stu-id="5b808-177">Clear the **Demo mode** field.</span></span> <br>

    <span data-ttu-id="5b808-178">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-178">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span></span>

3.  <span data-ttu-id="5b808-179">ป้อนข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5b808-179">Enter the following information:</span></span> 
    + <span data-ttu-id="5b808-180">**รหัสไคลของเอนต์ Azure Active directory** - รหัสของไคลเอนต์จะได้รับในขั้นตอนที่ 9 ใน "สร้างแอพบริการเว็บใน Active Directory"</span><span class="sxs-lookup"><span data-stu-id="5b808-180">**Azure Active directory client ID** - The client ID is obtained in step 9 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="5b808-181">**ข้อมูลลับไคลเอนต์ Azure Active directory** - ข้อมูลลับไคลเอนต์จะได้รับในขั้นตอนที่ 11 ใน "สร้างแอพบริการเว็บใน Active Directory"</span><span class="sxs-lookup"><span data-stu-id="5b808-181">**Azure Active directory client secret** - The client secret is obtained in step 11 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="5b808-182">**ทรัพยากร Azure Active directory** - ทรัพยากรไดเรกทอรี Azure AD แสดง URL รากของ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5b808-182">**Azure Active directory resource** - The Azure AD directory resource depicts the Supply Chain Managementroot URL.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="5b808-183">อย่าลงท้ายฟิลด์นี้ด้วยอักขระทับ (/)</span><span class="sxs-lookup"><span data-stu-id="5b808-183">Do not end this field with a forward slash character (/).</span></span> 

    + <span data-ttu-id="5b808-184">**ผู้เช่า Azure Active directory** - ผู้เช่าไดเรกทอรี Azure AD ที่ใช้กับเซิร์ฟเวอร์ Supply Chain Management: `https://login.windows.net/your-AD-tenant-ID`</span><span class="sxs-lookup"><span data-stu-id="5b808-184">**Azure Active directory tenant** - The Azure AD directory tenant used with the Supply Chain Management server: `https://login.windows.net/your-AD-tenant-ID`.</span></span> <span data-ttu-id="5b808-185">ตัวอย่างเช่น: `https://login.windows.net/contosooperations.onmicrosoft.com.`</span><span class="sxs-lookup"><span data-stu-id="5b808-185">For example: `https://login.windows.net/contosooperations.onmicrosoft.com.`</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="5b808-186">อย่าลงท้ายฟิลด์นี้ด้วยอักขระทับ (/)</span><span class="sxs-lookup"><span data-stu-id="5b808-186">Do not end this field with a forward slash character (/).</span></span> 
    
    + <span data-ttu-id="5b808-187">**บริษัท** - ป้อนนิติบุคคลใน Supply Chain Management ที่คุณต้องการให้แอพลิเคชันเชื่อมต่อด้วย</span><span class="sxs-lookup"><span data-stu-id="5b808-187">**Company** - Enter the legal entity in Supply Chain Management to which you want the application to connect.</span></span> <br>
    
    <span data-ttu-id="5b808-188">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-188">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span></span>

4.  <span data-ttu-id="5b808-189">เลือกปุ่ม **ย้อนกลับ** ที่มุมซ้ายด้านบนของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="5b808-189">Select the **Back** button in the top-left corner of the application.</span></span> <span data-ttu-id="5b808-190">ในขณะนี้แอพลิเคชันจะเชื่อมต่อกับเซิร์ฟเวอร์ Supply Chain Management ของคุณและระบบจะแสดงหน้าจอการเข้าสู่ระบบสำหรับผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="5b808-190">The application will now connect to your Supply Chain Management server and the log-in screen for the warehouse worker will display.</span></span>

    <span data-ttu-id="5b808-191">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span><span class="sxs-lookup"><span data-stu-id="5b808-191">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span></span>

<span data-ttu-id="5b808-192">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าแอพพลิเคชั่น Warehousing ที่จะสแกนบาร์โค้ดโดยใช้กล้องบนอุปกรณ์มือถือ ดู [สแกนบาร์โค้ดโดยใช้กล้องใน Dynamics 365 for Finance and Operations  - แอปคลังสินค้า](scan-bar-codes-using-a-camera.md)</span><span class="sxs-lookup"><span data-stu-id="5b808-192">For information on how to set up the Warehousing app to scan bar codes using a camera on a mobile device, see [Scan bar codes using a camera in Dynamics 365 for Finance and Operations - Warehousing app](scan-bar-codes-using-a-camera.md).</span></span>

## <a name="remove-access-for-a-device"></a><span data-ttu-id="5b808-193">ลบการเข้าถึงออกจากอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="5b808-193">Remove access for a device</span></span>
<span data-ttu-id="5b808-194">ในกรณีที่อุปกรณ์สูญหายหรือระบบถูกโจมตี คุณต้องลบการเข้าถึง Supply Chain Management ออกจากอุปกรณ์</span><span class="sxs-lookup"><span data-stu-id="5b808-194">In case of a lost or compromised device, you must remove access to Supply Chain Management for the device.</span></span> <span data-ttu-id="5b808-195">ขั้นตอนต่อไปนี้อธิบายกระบวนการที่แนะนำในการลบการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="5b808-195">The following steps describe the recommended process to remove access.</span></span>

1.  <span data-ttu-id="5b808-196">ไปที่ **การจัดการระบบ** &gt; **การตั้งค่า** &gt; แอพพลิเคชั่น **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="5b808-196">Go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
2.  <span data-ttu-id="5b808-197">ลบบรรทัดที่สอดคล้องกับอุปกรณ์ที่คุณต้องการลบการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="5b808-197">Delete the line that corresponds to the device to which you want to remove access.</span></span> <span data-ttu-id="5b808-198">อย่าลืม **รหัสไคลเอนต์** ที่ใช้สำหรับอุปกรณ์ที่ลบออก คุณจะต้องใช้ข้อมูลนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="5b808-198">Remember the **Client ID** used for the removed device, you will need it later.</span></span>
3.  <span data-ttu-id="5b808-199">ล็อกอินไปยังพอร์ทัล Azure ที่ <https://portal.azure.com></span><span class="sxs-lookup"><span data-stu-id="5b808-199">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
4.  <span data-ttu-id="5b808-200">คลิกไอคอน **Active Directory** บนเมนูซ้าย และให้แน่ใจว่าคุณอยู่ในไดเรกทอรีที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="5b808-200">Click the **Active Directory** icon on the left menu, and ensure that you are in the correct directory.</span></span>
5.  <span data-ttu-id="5b808-201">ในรายการ คลิก **การลงทะเบียนแอพ** แล้วคลิกแอพลิเคชันที่คุณต้องการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="5b808-201">In the list, click **App registrations**, and then click the application that you want to configure.</span></span> <span data-ttu-id="5b808-202">หน้า **การตั้งค่า** จะปรากฏขึ้นพร้อมด้วยข้อมูลการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="5b808-202">The **Settings** page will appear with configuration information.</span></span>
6.  <span data-ttu-id="5b808-203">ให้แน่ใจว่า **รหัสไคลเอนต์** ของแอพลิเคชันเหมือนกับในขั้นตอนที่ 2 ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="5b808-203">Ensure that the **Client ID** of the application is the same as in step 2 in this section.</span></span>
7.  <span data-ttu-id="5b808-204">คลิกปุ่ม **ลบ** ในบานหน้าต่างด้านบน</span><span class="sxs-lookup"><span data-stu-id="5b808-204">Click the **Delete** button in the top pane.</span></span>
8.  <span data-ttu-id="5b808-205">คลิก **ใช่** ในข้อความยืนยัน</span><span class="sxs-lookup"><span data-stu-id="5b808-205">Click **Yes** in the confirmation message.</span></span>
