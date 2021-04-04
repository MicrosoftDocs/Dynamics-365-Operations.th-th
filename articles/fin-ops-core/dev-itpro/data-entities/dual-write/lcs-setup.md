---
title: การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง จาก Microsoft Dynamics Lifecycle Services (LCS)
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567731"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="e4a90-103">การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e4a90-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e4a90-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางระหว่างสภาพแวดล้อม Finance and Operations ใหม่ และสภาพแวดล้อม Dataverse ใหม่จาก Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e4a90-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4a90-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="e4a90-105">Prerequisites</span></span>

<span data-ttu-id="e4a90-106">คุณต้องเป็นผู้ดูแลระบบจึงจะสามารถตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางได้</span><span class="sxs-lookup"><span data-stu-id="e4a90-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="e4a90-107">คุณต้องมีการเข้าถึงผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="e4a90-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="e4a90-108">คุณต้องเป็นผู้ดูแลระบบทั้งในสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="e4a90-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="e4a90-109">ตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="e4a90-109">Set up a dual-write connection</span></span>

<span data-ttu-id="e4a90-110">ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="e4a90-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="e4a90-111">ใน LCS ไปที่โครงการของคุณ</span><span class="sxs-lookup"><span data-stu-id="e4a90-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="e4a90-112">เลือก **ตั้งค่าคอนฟิก** เพื่อปรับใช้สภาพแวดล้อมใหม่</span><span class="sxs-lookup"><span data-stu-id="e4a90-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="e4a90-113">เลือกรุ่น</span><span class="sxs-lookup"><span data-stu-id="e4a90-113">Select the version.</span></span> 
4. <span data-ttu-id="e4a90-114">เลือกโทโพโลยี</span><span class="sxs-lookup"><span data-stu-id="e4a90-114">Select the topology.</span></span> <span data-ttu-id="e4a90-115">ถ้ามีหนึ่งโทโพโลยีเท่านั้นที่พร้อมใช้งาน จะมีการเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e4a90-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="e4a90-116">ปฏิบัติตามขั้นตอนแรกในวิซาร์ด **การตั้งค่าการปรับใช้** ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e4a90-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="e4a90-117">บนแท็บ **Dataverse** ทำตามหนึ่งในขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="e4a90-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="e4a90-118">ถ้ามีการเตรียมใช้งานสภาพแวดล้อม Dataverse สำหรับผู้เช่าของคุณแล้ว คุณสามารถเลือกสภาพแวดล้อมได้</span><span class="sxs-lookup"><span data-stu-id="e4a90-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="e4a90-119">ตั้งค่าตัวเลือก **ตั้งค่าคอนฟิก Dataverse** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e4a90-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="e4a90-120">ในคอลัมน์ **สภาพแวดล้อมที่พร้อมใช้งาน** ให้เลือกสภาพแวดล้อมที่จะรวมกับข้อมูล Finance and Operations ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e4a90-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="e4a90-121">รายการนี้รวมถึงสภาพแวดล้อมทั้งหมดที่ซึ่งคุณมีสิทธิ์ของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e4a90-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="e4a90-122">เลือกกล่องกาเครื่องหมาย **ยินยอม** เพื่อระบุว่าคุณยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="e4a90-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![แท็บ Dataverse เมื่อมีการเตรียมใช้งานสภาพแวดล้อม Dataverse สำหรับผู้เช่าของคุณแล้ว](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="e4a90-124">ถ้าผู้เช่าของคุณไม่มีสภาพแวดล้อม Dataverse สภาพแวดล้อมใหม่จะถูกเตรียมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e4a90-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="e4a90-125">ตั้งค่าตัวเลือก **ตั้งค่าคอนฟิก Dataverse** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="e4a90-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="e4a90-126">ป้อนชื่อสำหรับสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="e4a90-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="e4a90-127">เลือกภูมิภาคที่จะปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="e4a90-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="e4a90-128">เลือกภาษาและสกุลเงินเริ่มต้นสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="e4a90-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="e4a90-129">คุณไม่สามารถเปลี่ยนภาษาและสกุลเงินในภายหลังได้</span><span class="sxs-lookup"><span data-stu-id="e4a90-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="e4a90-130">เลือกกล่องกาเครื่องหมาย **ยินยอม** เพื่อระบุว่าคุณยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="e4a90-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![แท็บ Dataverse เมื่อผู้เช่าของคุณไม่มีสภาพแวดล้อม Dataverse อยู่แล้ว](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="e4a90-132">ปฏิบัติตามขั้นตอนที่เหลือในวิซาร์ด **การตั้งค่าการปรับใช้** ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e4a90-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="e4a90-133">หลังจากที่สภาพแวดล้อมมีสถานะเป็น **ปรับใช้แล้ว** ให้เปิดหน้ารายละเอียดของสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="e4a90-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="e4a90-134">ส่วน **การรวม Power Platform** แสดงชื่อของสภาพแวดล้อม Finance and Operations และสภาพแวดล้อม Dataverse ที่มีการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="e4a90-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![ส่วนการรวม Power Platform](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="e4a90-136">ผู้ดูแลระบบของสภาพแวดล้อม Finance and Operations ต้องลงชื่อเข้าใช้ใน LCS และเลือก **ลิงค์ไปยัง CDS for Apps** เพื่อทำให้การเชื่อมโยงเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e4a90-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="e4a90-137">หน้ารายละเอียดของสภาพแวดล้อมจะแสดงข้อมูลผู้ติดต่อของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e4a90-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="e4a90-138">หลังจากเสร็จสิ้นการเชื่อมโยง สถานะจะได้รับการอัพเดตเป็น **การเชื่อมโยงสภาพแวดล้อมเสร็จเรียบร้อยแล้ว**</span><span class="sxs-lookup"><span data-stu-id="e4a90-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="e4a90-139">เมื่อต้องการเปิดพื้นที่ทำงาน **การรวมข้อมูล** ในสภาพแวดล้อม Finance and Operations และควบคุมเท็มเพลตที่พร้อมใช้งาน เลือก **เชื่อมโยงกับ CDS for Apps**</span><span class="sxs-lookup"><span data-stu-id="e4a90-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![ปุ่มลิงค์ไปยัง CDS for Apps ในส่วนการรวม Power Platform](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="e4a90-141">คุณไม่สามารถยกเลิกการเชื่อมโยงสภาพแวดล้อมได้โดยใช้ LCS</span><span class="sxs-lookup"><span data-stu-id="e4a90-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="e4a90-142">เมื่อต้องการยกเลิกการเชื่อมโยงสภาพแวดล้อม ให้เปิดพื้นที่ทำงาน **การรวมข้อมูล** ในสภาพแวดล้อม Finance and Operations และจากนั้น เลือก **ยกเลิกการเชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="e4a90-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]