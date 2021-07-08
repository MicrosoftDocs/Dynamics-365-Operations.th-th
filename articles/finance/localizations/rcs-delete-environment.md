---
title: Regulatory Configuration Service (RCS) - ลบสภาพแวดล้อม RCS
description: หัวข้อนี้อธิบายวิธีการที่ผู้ดูแลระบบ Regulatory Configuration Service (RCS) สามารถลบสภาพแวดล้อม RCS และข้อมูลที่เกี่ยวข้องได้
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295829"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="a6582-103">Regulatory Configuration Service (RCS) - ลบสภาพแวดล้อม RCS</span><span class="sxs-lookup"><span data-stu-id="a6582-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6582-104">หัวข้อนี้อธิบายวิธีการที่ผู้ดูแลระบบ Regulatory Configuration Service (RCS) สามารถลบสภาพแวดล้อม RCS และข้อมูลที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="a6582-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="a6582-105">ก่อนที่คุณจะสามารถดำเนินการกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ ต้องตรงข้อกำหนดเบื้องต้นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6582-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="a6582-106">คุณต้องได้รับมอบหมายบทบาท **ผู้ดูแลระบบ** ให้กับคุณให้กับสภาพแวดล้อม RCS</span><span class="sxs-lookup"><span data-stu-id="a6582-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="a6582-107">บทบาท **ผู้ดูแลระบบ** ต้องมอบหมายบทบาท **RCSDeleteEnvironmentDuty** ให้กับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="a6582-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="a6582-108">ลบสภาพแวดล้อม RCS</span><span class="sxs-lookup"><span data-stu-id="a6582-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="a6582-109">เปิด RCS และให้เลือกไทล์พื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a6582-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="a6582-110">ในส่วน **ลิงค์ที่เกี่ยวข้อง** ให้เลือก **ลบสภาพแวดล้อม RCS**</span><span class="sxs-lookup"><span data-stu-id="a6582-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![ลบลิงค์สภาพแวดล้อม RCS ในส่วนลิงค์ที่เกี่ยวข้อง](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="a6582-112">ในกล่องโต้ตอบที่ปรากฏ ให้ทบทวนข้อความเกี่ยวกับขอบเขตของการลบสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="a6582-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![ข้อความในกล่องโต้ตอบลบสภาพแวดล้อม RCS](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="a6582-114">ไม่สามารถกลับรายการการลบสภาพแวดล้อม RCS</span><span class="sxs-lookup"><span data-stu-id="a6582-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="a6582-115">การดําเนินงานจะลบสภาพแวดล้อม RCS ที่เลือกและข้อมูลที่เกี่ยวข้องใดๆ รวมถึงลักษณะการดําเนินการและการตั้งค่าคอนฟิกที่จัดเก็บอยู่ในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="a6582-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="a6582-116">คุณลักษณะและการตั้งค่าคอนฟิกที่ใช้ร่วมกันกับองค์กรอื่นๆ จะถูกยกเลิกและลบออกถ้าไม่มีการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="a6582-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="a6582-117">คุณลักษณะและการตั้งค่าคอนฟิกที่ขึ้นต่อกันจะถูกเลือกเป็นถูกตัดออก</span><span class="sxs-lookup"><span data-stu-id="a6582-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="a6582-118">ในฟิลด์ที่ระบุ ให้ป้อนรหัสเฉพาะสากล (GUID) ของสภาพแวดล้อม RCS เพื่อยืนยันว่าคุณต้องการลบ</span><span class="sxs-lookup"><span data-stu-id="a6582-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="a6582-119">GUID ของสภาพแวดล้อมรวมอยู่ในข้อความลบ</span><span class="sxs-lookup"><span data-stu-id="a6582-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="a6582-120">เลือก **ลบสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="a6582-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="a6582-121">ขณะนี้สภาพแวดล้อม RCS และข้อมูลที่เกี่ยวข้องใดๆ ของคุณถูกลบแล้ว</span><span class="sxs-lookup"><span data-stu-id="a6582-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6582-122">หลังจากที่คุณลบสภาพแวดล้อม RCS แล้ว จะไม่มีวิธีกู้คืนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a6582-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="a6582-123">คุณสามารถสร้างสภาพแวดล้อม RCS ใหม่ได้ในภูมิภาค RCS ที่พร้อมใช้งานใดๆ</span><span class="sxs-lookup"><span data-stu-id="a6582-123">A new RCS environment can be created in any available RCS region.</span></span>
