---
title: เตรียมใช้งานสภาพแวดล้อมการประเมิน Dynamics 365 Commerce
description: หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19cedf01d1b916de785454d55448f41d1f5db1df
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792302"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="85208-103">เตรียมใช้งานสภาพแวดล้อมการประเมิน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="85208-104">หัวข้อนี้อธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมการประเมินของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="85208-105">ก่อนที่คุณจะเริ่มต้น เราขอแนะนำให้คุณอ่านผ่านหัวข้อนี้เพื่อดูว่ากระบวนการต้องใช้อะไร</span><span class="sxs-lookup"><span data-stu-id="85208-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="85208-106">สภาพแวดล้อมการประเมิน Commerce โดยทั่วไปไม่พร้อมใช้งาน และจะถูกกำหนดให้กับคู่ค้าและลูกค้าในแต่ละคำขอ</span><span class="sxs-lookup"><span data-stu-id="85208-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="85208-107">สำหรับข้อมูลเพิ่มเติม ติดต่อคู่ค้า Microsoft ของคุณ</span><span class="sxs-lookup"><span data-stu-id="85208-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="85208-108">เพื่อเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce ให้สำเร็จ คุณต้องสร้างโครงการที่มีชื่อและชนิดของผลิตภัณฑ์ที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="85208-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="85208-109">นอกจากนี้ สภาพแวดล้อมและ Commerce Scale Unit (CSU) ยังมีพารามิเตอร์เฉพาะบางอย่างที่คุณต้องใช้ เมื่อคุณคาดว่าจะเตรียมใช้งานอีคอมเมิร์ซในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="85208-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="85208-110">คำแนะนำในหัวข้อนี้อธิบายขั้นตอนที่จำเป็นทั้งหมดที่คุณต้องทำการเตรียมใช้งานให้เสร็จสมบูรณ์ และพารามิเตอร์ที่คุณต้องใช้</span><span class="sxs-lookup"><span data-stu-id="85208-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="85208-111">หลังจากที่คุณเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce ของคุณเสร็จสิ้น คุณต้องดำเนินการขั้นตอนหลังการเตรียมใช้งานสองสามขั้นตอนเพื่อจัดเตรียมสำหรับการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85208-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="85208-112">ขั้นตอนบางอย่างอาจไม่จำเป็น ขึ้นอยู่กับแง่มุมของระบบที่คุณต้องการประเมิน</span><span class="sxs-lookup"><span data-stu-id="85208-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="85208-113">คุณสามารถดำเนินการตามขั้นตอนที่ไม่จำเป็นในภายหลังได้เสมอ</span><span class="sxs-lookup"><span data-stu-id="85208-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="85208-114">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Commerce ของคุณ หลังจากที่คุณเตรียมใช้งาน ให้ดูที่ [ตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Commerce](cpe-post-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="85208-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="85208-115">สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Commerce ของคุณ ให้ดูที่ [ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Commerce](cpe-optional-features.md)</span><span class="sxs-lookup"><span data-stu-id="85208-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85208-116">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="85208-116">Prerequisites</span></span>

<span data-ttu-id="85208-117">ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้ ก่อนที่คุณจะสามารถเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce ของคุณได้:</span><span class="sxs-lookup"><span data-stu-id="85208-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="85208-118">คุณได้รับการเตรียมความพร้อมไปยังโปรแกรมการประเมินและได้รับกำลังการผลิตสำหรับสภาพแวดล้อมการประเมิน</span><span class="sxs-lookup"><span data-stu-id="85208-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="85208-119">คุณมีสิทธิ์เข้าถึงพอร์ทัล Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="85208-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="85208-120">คุณเป็นคู่ค้าหรือลูกค้า Microsoft Dynamics 365 แล้ว และสามารถสร้างโครงการ Dynamics 365 Commerce ได้</span><span class="sxs-lookup"><span data-stu-id="85208-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="85208-121">คุณสามารถมีการเข้าถึงของผู้ดูแลระบบไปยังการบอกรับเป็นสมาชิก Microsoft Azure ของคุณ หรือคุณติดต่อกับผู้ดูแลการบอกรับเป็นสมาชิกซึ่งสามารถช่วยเหลือคุณได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="85208-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="85208-122">คุณมีรหัสผู้เช่า Azure Active Directory (Azure AD) ของคุณที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85208-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="85208-123">คุณได้สร้างกลุ่มรักษาความปลอดภัย Azure AD ที่สามารถใช้เป็นกลุ่มผู้ดูแลระบบอีคอมเมิร์ซ และคุณมีรหัสที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85208-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="85208-124">คุณได้สร้างกลุ่มรักษาความปลอดภัย Azure AD ที่สามารถใช้เป็นกลุ่มผู้ดูแลการให้คะแนนและบทวิจารณ์ และคุณมีรหัสที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85208-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="85208-125">(กลุ่มความปลอดภัยนี้อาจเหมือนกับกลุ่มผู้ดูแลระบบพาณิชย์อิเล็กทรอนิกส์)</span><span class="sxs-lookup"><span data-stu-id="85208-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="85208-126">โปรดทราบว่ารายการนี้ยังไม่ครอบคลุมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="85208-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="85208-127">หากคุณพบปัญหาใดๆ ให้ติดต่อคู่ค้า Microsoft ของคุณสำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="85208-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="85208-128">เตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="85208-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="85208-129">กระบวนงานเหล่านี้จะอธิบายวิธีการเตรียมใช้งานสภาพแวดล้อมการประเมินของ Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="85208-130">หลังจากที่คุณดำเนินการเสร็จสมบูรณ์แล้ว สภาพแวดล้อมการประเมินของ Commerce จะพร้อมสำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="85208-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="85208-131">กิจกรรมทั้งหมดที่อธิบายไว้ที่นี่จะเกิดขึ้นในพอร์ทัล LCS</span><span class="sxs-lookup"><span data-stu-id="85208-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="85208-132">สร้างโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="85208-132">Create a new project</span></span>

<span data-ttu-id="85208-133">เมื่อต้องการสร้างโครงการใหม่ใน LCS ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85208-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="85208-134">บนโฮมเพจ LCS ให้เลือกเครื่องหมายบวก (**+**) เพื่อสร้างโครงการ</span><span class="sxs-lookup"><span data-stu-id="85208-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="85208-135">ในบานหน้าต่างด้านขวา ให้ทำตามหนึ่งในขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="85208-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="85208-136">ถ้าคุณเป็นคู่ค้า ให้เลือก **โยกย้าย สร้างวิธีแก้ไข และเรียนรู้**</span><span class="sxs-lookup"><span data-stu-id="85208-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="85208-137">ถ้าคุณเป็นลูกค้า ให้เลือก **การเปิดจำหน่ายล่วงหน้าสำหรับผู้ที่มีแนวโน้มจะเป็นลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="85208-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="85208-138">ป้อนชื่อ คำอธิบาย และอุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="85208-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="85208-139">ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้เลือก **Dynamics 365 Commerce**</span><span class="sxs-lookup"><span data-stu-id="85208-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="85208-140">ในฟิลด์ **รุ่นผลิตภัณฑ์** ให้เลือก **Dynamics 365 Commerce**</span><span class="sxs-lookup"><span data-stu-id="85208-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="85208-141">ในฟิลด์ **วิธีการ** ให้เลือก **วิธีการใช้งานการขายปลีกของ Dynamics**</span><span class="sxs-lookup"><span data-stu-id="85208-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="85208-142">ไม่จำเป็นต้องระบุ: คุณสามารถนำเข้าบทบาทและผู้ใช้จากโครงการที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="85208-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="85208-143">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="85208-143">Select **Create**.</span></span> <span data-ttu-id="85208-144">มุมมองโครงการจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="85208-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="85208-145">เพิ่มตัวเชื่อมต่อ Azure</span><span class="sxs-lookup"><span data-stu-id="85208-145">Add the Azure Connector</span></span>

<span data-ttu-id="85208-146">เมื่อต้องการเพิ่มตัวเชื่อมต่อ Azure ไปยังโครงการ LCS ของคุณ ให้ทำตามขั้นตอนใน [ดำเนินการกระบวนการเตรียมความพร้อมของ Azure Resource Manager (ARM) ให้เสร็จสมบูรณ์](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding)</span><span class="sxs-lookup"><span data-stu-id="85208-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="85208-147">ปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="85208-147">Deploy the environment</span></span>

<span data-ttu-id="85208-148">เพื่อปรับใช้สภาพแวดล้อม ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85208-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="85208-149">คุณอาจไม่จำเป็นต้องทำตามขั้นตอนที่ 6 7 และ/หรือ 8 ให้เสร็จสมบูรณ์ เนื่องจากเพจที่มีตัวเลือกเดียวจะถูกข้ามไป</span><span class="sxs-lookup"><span data-stu-id="85208-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="85208-150">เมื่อคุณอยู่ในมุมมอง **พารามิเตอร์สภาพแวดล้อม** ให้ยืนยันว่าข้อความ **Dynamics 365 Commerce - สาธิต (10.0.* x* ที่มีการอัพเดตแพลตฟอร์ม *xx*)\*\* จะปรากฏขึ้นเหนือฟิลด์ **ชื่อสภาพแวดล้อม** โดยตรง</span><span class="sxs-lookup"><span data-stu-id="85208-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="85208-151">สำหรับรายละเอียด ให้ดูภาพประกอบที่ปรากฏหลังจากขั้นตอนที่ 8</span><span class="sxs-lookup"><span data-stu-id="85208-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="85208-152">บนเมนูด้านบน ให้เลือก **สภาพแวดล้อมที่ใช้ Cloud**</span><span class="sxs-lookup"><span data-stu-id="85208-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="85208-153">เลือก **เพิ่ม** เพื่อเพิ่มสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="85208-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="85208-154">ในฟิลด์ **รุ่นของแอพลิเคชัน** ให้เลือกเวอร์ชันที่เป็นปัจจุบันมากที่สุด</span><span class="sxs-lookup"><span data-stu-id="85208-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="85208-155">ถ้าคุณต้องเลือกรุ่นของแอพลิเคชันอื่นที่ไม่ใช่เวอร์ชันที่เป็นปัจจุบันมากที่สุด อย่าเลือกรุ่นก่อนหน้ารุ่น **10.0.14**</span><span class="sxs-lookup"><span data-stu-id="85208-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="85208-156">ในฟิลด์ **เวอร์ชันของแพลตฟอร์ม** ให้ใช้เวอร์ชันของแพลตฟอร์มที่เลือกโดยอัตโนมัติสำหรับเวอร์ชันของแอพลิเคชันที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="85208-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![การเลือกรุ่นของแอพลิเคชันและแพลตฟอร์ม](./media/project1.png)

1. <span data-ttu-id="85208-158">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="85208-158">Select **Next**.</span></span>
1. <span data-ttu-id="85208-159">เลือก **สาธิต** เป็นโทโพโลยีสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="85208-159">Select **Demo** as the environment topology.</span></span>

    ![การเลือกโทโพโลยีสภาพแวดล้อม 1](./media/project2.png)

1. <span data-ttu-id="85208-161">บนเพจ **ปรับใช้สภาพแวดล้อม** ให้ป้อนชื่อสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="85208-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="85208-162">ปล่อยการตั้งค่าขั้นสูงไว้ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="85208-162">Leave the advanced settings as they are.</span></span>

    ![ปรับใช้เพจสภาพแวดล้อม](./media/project4.png)

1. <span data-ttu-id="85208-164">ปรับขนาด VM ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="85208-164">Adjust the VM size as required.</span></span> <span data-ttu-id="85208-165">(เราขอแนะนำหน่วยการเก็บสต็อกสินค้า VM \[SKU\] **D13 v2**)</span><span class="sxs-lookup"><span data-stu-id="85208-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="85208-166">ตรวจสอบเงื่อนไขการกำหนดราคาและการให้สิทธิ์การใช้งาน และจากนั้น เลือกกล่องกาเครื่องหมายเพื่อบ่งชี้ว่าคุณเห็นด้วย</span><span class="sxs-lookup"><span data-stu-id="85208-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="85208-167">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="85208-167">Select **Next**.</span></span>
1. <span data-ttu-id="85208-168">บนหน้ายืนยันการปรับใช้ ตรวจสอบว่ารายละเอียดทั้งหลายถูกต้อง และจากนั้น เลือก **ปรับใช้**</span><span class="sxs-lookup"><span data-stu-id="85208-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="85208-169">คุณจะกลับไปยังมุมมอง **สภาพแวดล้อมที่ใช้ Cloud** และสภาพแวดล้อมของคุณควรจะปรากฏในรายการ</span><span class="sxs-lookup"><span data-stu-id="85208-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="85208-170">สภาพแวดล้อมที่ร้องขอของคุณจะปรากฎเป็นอยู่ในคิว และจากนั้นจะเปลี่ยนเป็นกำลังปรับใช้</span><span class="sxs-lookup"><span data-stu-id="85208-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="85208-171">เวิร์กโฟลว์สภาพแวดล้อมจะใช้เวลาสักครู่เพื่อให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="85208-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="85208-172">ดังนั้น โปรดกลับมาตรวจสอบหลังจากประมาณหกถึงเก้าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="85208-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="85208-173">ก่อนที่คุณจะดำเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าสถานะของสภาพแวดล้อมของคุณคือ **ปรับใช้แล้ว**</span><span class="sxs-lookup"><span data-stu-id="85208-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="85208-174">เริ่มต้น Commerce Scale Unit (ระบบคลาวด์)</span><span class="sxs-lookup"><span data-stu-id="85208-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="85208-175">เมื่อต้องการเริ่มต้น CSU ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85208-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="85208-176">ในมุมมอง **สภาพแวดล้อมที่ใช้ Cloud** ให้เลือกสภาพแวดล้อมของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="85208-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="85208-177">ในมุมมองสภาพแวดล้อมทางด้านขวา เลือก **รายละเอียดแบบเต็ม**</span><span class="sxs-lookup"><span data-stu-id="85208-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="85208-178">มุมมองรายละเอียดของสภาพแวดล้อมจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="85208-178">The environment details view appears.</span></span>
1. <span data-ttu-id="85208-179">ภายใต้ **คุณลักษณะของสภาพแวดล้อม** ให้เลือก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="85208-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="85208-180">บนแท็บ **Commerce** ให้เลือก **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="85208-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="85208-181">มุมมองพารามิเตอร์สำหรับการเริ่มต้นใช้งาน CSU จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="85208-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="85208-182">ในฟิลด์ **ภูมิภาค** ให้เลือกภูมิภาคที่เหมือนกันหรือใกล้เคียงกับภูมิภาคที่คุณปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="85208-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="85208-183">ปล่อยฟิลด์ **รุ่น** ตามที่เป็นอยู่</span><span class="sxs-lookup"><span data-stu-id="85208-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="85208-184">เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="85208-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="85208-185">บนหน้ายืนยันการปรับใช้ ตรวจสอบว่ารายละเอียดทั้งหลายถูกต้อง และจากนั้น เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="85208-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="85208-186">มุมมอง **การจัดการ Commerce** จะแสดงอีกครั้งโดยที่แท็บ **Commerce** จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="85208-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="85208-187">CSU ของคุณได้รับการจัดคิวสำหรับการเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="85208-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="85208-188">ก่อนที่คุณจะดำเนินการต่อ โปรดตรวจสอบให้แน่ใจว่าสถานะของ CSU ของคุณคือ **สำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="85208-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="85208-189">การเริ่มต้นใช้งานจะใช้เวลาประมาณสองถึงห้าชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="85208-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="85208-190">ถ้าคุณไม่พบลิงค์ **จัดการ** ในมุมมองรายละเอียดของสภาพแวดล้อม โปรดติดต่อผู้ติดต่อ Microsoft ของคุณสำหรับความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="85208-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="85208-191">ในระหว่างกระบวนการปรับใช้ คุณอาจได้รับข้อความแสดงข้อผิดพลาด:</span><span class="sxs-lookup"><span data-stu-id="85208-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="85208-192">สภาพแวดล้อมการประเมิน (สาธิต/ทดสอบ) ต้องลงทะเบียนแอปพลิเคชันตัวเชื่อมต่อหน่วย scale unit \<application ID\> ในศูนย์ควบคุม</span><span class="sxs-lookup"><span data-stu-id="85208-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="85208-193">หากการเริ่มต้น CSU ล้มเหลวและคุณได้รับข้อความแสดงข้อผิดพลาดนี้ ให้บันทึกรหัสแอปพลิเคชันซึ่งเป็นรหัสเฉพาะสากล (GUID) แล้วปฏิบัติตามขั้นตอนในส่วนถัดไปเพื่อลงทะเบียนแอปพลิเคชันการปรับใช้ CSU ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="85208-194">ลงทะเบียนแอปพลิเคชันการปรับใช้ CSU ในศูนย์ควบคุม Commerce (ถ้าต้องใช้)</span><span class="sxs-lookup"><span data-stu-id="85208-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="85208-195">หากต้องการลงทะเบียนแอปพลิเคชันการปรับใช้ CSU ในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="85208-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="85208-196">ในศูนย์ควบคุม Commerce ให้ไปที่ **การจัดการระบบ \> การตั้งค่า \> แอปพลิเคชัน Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="85208-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="85208-197">ในคอลัมน์ **รหัสไคลเอนต์** ให้ป้อนรหัสแอปพลิเคชันจากข้อความแสดงข้อผิดพลาดการเริ่มต้น CSU ที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="85208-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="85208-198">ในคอลัมน์ **ชื่อ** ให้ป้อนข้อความอธิบายใด ๆ (ตัวอย่างเช่น **CSU Eval)**</span><span class="sxs-lookup"><span data-stu-id="85208-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="85208-199">ในคอลัมน์ **รหัสผู้ใช้** ให้ป้อน **RetailServiceAccount**</span><span class="sxs-lookup"><span data-stu-id="85208-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="85208-200">ลองเริ่มต้น CSU และการปรับใช้จาก LCS อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="85208-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="85208-201">ตั้งค่าเพื่อเริ่มต้นใช้งานอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="85208-201">Initialize e-Commerce</span></span>

<span data-ttu-id="85208-202">เมื่อต้องการเริ่มต้นอีคอมเมิร์ซ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="85208-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="85208-203">บนแท็บ **อีคอมเมิร์ซ** ให้รีวิวความยินยอมในการประเมิน และจากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="85208-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="85208-204">ในฟิลด์ **ชื่อสภาพแวดล้อมอีคอมเมิร์ซ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="85208-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="85208-205">โปรดทราบว่าชื่อนี้จะปรากฏในบาง URL ที่ชี้ไปยังอินสแตนซ์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="85208-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="85208-206">ในฟิลด์ **ชื่อ Commerce Scale Unit** เลือก CSU ของคุณในรายการ</span><span class="sxs-lookup"><span data-stu-id="85208-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="85208-207">(รายการควรมีเพียงตัวเลือกเดียว)</span><span class="sxs-lookup"><span data-stu-id="85208-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="85208-208">ฟิลด์ **ภูมิศาสตร์ของอีคอมเมิร์ซ** ถูกตั้งค่าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="85208-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="85208-209">เลือก **ถัดไป** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="85208-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="85208-210">ในฟิลด์ **ชื่อโฮสต์ที่ได้รับการสนับสนุน** ให้ป้อนโดเมนที่ถูกต้องใดๆ เช่น `www.fabrikam.com`</span><span class="sxs-lookup"><span data-stu-id="85208-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="85208-211">ในฟิลด์ **กลุ่มรักษาความปลอดภัย AAD สำหรับผู้ดูแลระบบ** ให้ป้อนตัวอักษรสองสามตัวแรกของชื่อกลุ่มรักษาความปลอดภัยที่คุณต้องการใช้ แล้วจากนั้น เลือกสัญลักษณ์แว่นขยายเพื่อดูผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="85208-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="85208-212">เลือกกลุ่มความปลอดภัยที่ถูกต้องในรายการ</span><span class="sxs-lookup"><span data-stu-id="85208-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="85208-213">ในฟิลด์ **กลุ่มรักษาความปลอดภัย AAD สำหรับการให้คะแนนและรีวิวผู้ตรวจสอบ** ให้ป้อนตัวอักษรสองสามตัวแรกของชื่อกลุ่มรักษาความปลอดภัยที่คุณต้องการใช้ แล้วจากนั้น เลือกสัญลักษณ์แว่นขยายเพื่อดูผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="85208-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="85208-214">เลือกกลุ่มความปลอดภัยที่ถูกต้องในรายการ</span><span class="sxs-lookup"><span data-stu-id="85208-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="85208-215">ปล่อยให้ตัวเลือก **เปิดใช้งานการให้คะแนนและรีวิวบริการ** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="85208-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="85208-216">เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="85208-216">Select **Initialize**.</span></span> <span data-ttu-id="85208-217">มุมมอง **การจัดการ Commerce** จะแสดงอีกครั้งโดยที่แท็บ **อีคอมเมิร์ซ** จะถูกเลือก</span><span class="sxs-lookup"><span data-stu-id="85208-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="85208-218">การเริ่มใช้งานอีคอมเมิร์ซได้เริ่มต้นขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="85208-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="85208-219">ก่อนที่คุณจะดำเนินการต่อไป ให้รอจนกว่าสถานะของการเริ่มต้นใช้งานอีคอมเมิร์ซจะเป็น **การเริ่มต้นใช้งานสำเร็จ**</span><span class="sxs-lookup"><span data-stu-id="85208-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="85208-220">ภายใต้ **ลิงค์** ที่ด้านล่างขวา ให้จดบันทึก URL สำหรับลิงค์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="85208-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="85208-221">**ไซต์อีคอมเมิร์ซ** – การเชื่อมโยงไปยังรากของไซต์อีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="85208-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="85208-222">**ตัวสร้างไซต์ Commerce** – การเชื่อมโยงไปยังเครื่องมือการจัดการไซต์</span><span class="sxs-lookup"><span data-stu-id="85208-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="85208-223">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="85208-223">Next steps</span></span>

<span data-ttu-id="85208-224">เพื่อดำเนินการกระบวนการในการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Commerce ของคุณต่อ ให้ดูที่ [ตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Commerce](cpe-post-provisioning.md)</span><span class="sxs-lookup"><span data-stu-id="85208-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85208-225">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="85208-225">Additional resources</span></span>

[<span data-ttu-id="85208-226">ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="85208-227">ตั้งค่าคอนฟิกภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="85208-228">ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="85208-229">ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="85208-230">FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="85208-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="85208-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="85208-232">Commerce Scale Unit (ระบบคลาวด์)</span><span class="sxs-lookup"><span data-stu-id="85208-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="85208-233">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="85208-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="85208-234">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="85208-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
