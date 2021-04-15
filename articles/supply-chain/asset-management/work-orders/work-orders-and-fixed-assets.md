---
title: ใบสั่งงานและสินทรัพย์ถาวร
description: หัวข้อนี้อธิบายใบสั่งงาน เเละสินทรัพย์ถาวรในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65adcd07f1649b2e4eb2e2528507bb15631782ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816735"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="84ac6-103">ใบสั่งงานและสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="84ac6-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="84ac6-104">ในการจัดการสินทรัพย์ สินทรัพย์สามารถเกี่ยวข้องกับสินทรัพย์ถาวร เเละคุณสามารถสร้างใบสั่งงานสำหรับสินทรัพย์เหล่านั่นได้</span><span class="sxs-lookup"><span data-stu-id="84ac6-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="84ac6-105">ถ้าคุณใช้ฟังก์ชันนี้ คุณจะได้รับภาพรวมของสินทรัพย์ถาวร โครงการลงทุนที่เกี่ยวข้อง และต้นทุนที่ลงทะเบียนบนโครงการลงทุนในโมดูล **การจัดการโครงการเเละการบัญชี** เเละโมดูล **สินทรัพย์ถาวร** ใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="84ac6-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="84ac6-106">ฟิลด์ **หมายเลขสินทรัพย์ถาวร** บนโครงการงานใบสั่งงานถูกตั้งค่าก็ต่อเมื่อ **การลงทุน** ถูกเลือกเป็นชนิดโครงการบนโครงการงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="84ac6-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="84ac6-107">ภาพประกอบด้านล่างแสดงความสัมพันธ์ระหว่างโครงการลงทุนในโมดูล **การจัดการโครงการและการบัญชี** และโครงการงานใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="84ac6-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![รูปที่ 1](media/24-work-orders.png)

<span data-ttu-id="84ac6-109">กระบวนงานต่อไปนี้จะอธิบายความสัมพันธ์ระหว่างสินทรัพย์ ใบสั่งงาน โครงการงานใบสั่งงาน และสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="84ac6-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="84ac6-110">คุณสร้างสินทรัพย์ที่คุณเชื่อมโยงกับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="84ac6-110">You create an asset that you relate to a fixed asset.</span></span>

![รูปที่ 2](media/25-work-orders.png)

2. <span data-ttu-id="84ac6-112">เมื่อคุณตั้งค่าชนิดของใบสั่งงานบนหน้า **ชนิดใบสั่งงาน** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **ชนิดใบสั่งงาน**) คุณสร้างชนิดใบสั่งงานสำหรับการจัดการการลงทุน</span><span class="sxs-lookup"><span data-stu-id="84ac6-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="84ac6-113">ดูเพิ่มเติมที่ [ชนิดใบสั่งงาน](../setup-for-work-orders/work-order-types.md)</span><span class="sxs-lookup"><span data-stu-id="84ac6-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![รูปที่ 3](media/26-work-orders.png)

3. <span data-ttu-id="84ac6-115">เมื่อคุณตั้งค่ากลุ่มโครงการของใบสั่งงานบนแท็บ **กลุ่มโครงการ** ของหน้า **การตั้งค่าโครงการของใบสั่งงาน** (**การจัดการสินทรัพย์** > **การตั้งค่า** > **ใบสั่งงาน** > **การตั้งค่าโครงการ**) คุณสร้างความสัมพันธ์ระหว่างชนิดของใบสั่งงานที่ใช้สำหรับการลงทุน และกลุ่มโครงการที่ถูกสร้างสำหรับการลงทุนบนหน้า **กลุ่มโครงการ** ในโมดูล **การจัดการโครงการเเละการบัญชี** (**การจัดการโครงการเเละการบัญชี** > **การตั้งค่า** > **การลงรายการบัญชี** > **กลุ่มโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="84ac6-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![รูปที่ 4](media/27-work-orders.png)

4. <span data-ttu-id="84ac6-117">เมื่อคุณสร้างใบสั่งงานที่เกี่ยวข้องกับสินทรัพย์ถาวร คุณเลือกชนิดของใบสั่งงานที่ใช้เพื่อจัดการการลงทุน เช่น **การลงทุน**</span><span class="sxs-lookup"><span data-stu-id="84ac6-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="84ac6-118">เมื่อใบสั่งงานถูกสร้าง ชนิดใบสั่งงานที่เกี่ยวข้องจะเเสดงขึ้นในหน้า **ใบสั่งงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="84ac6-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![รูปที่ 5](media/28-work-orders.png)

6. <span data-ttu-id="84ac6-120">เมื่อใบสั่งงานถูกสร้าง โครงการที่เกี่ยวข้องกับใบสั่งงานจะถูกสร้างขึ้นบนหน้า **โครงการทั้งหมด** ในโมดูล **การจัดการโครงการและการบัญชี** (**การจัดการโครงการและการบัญชี** > **โครงการ** > **โครงการทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="84ac6-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="84ac6-121">เมื่อต้องการดูข้อมูลที่เกี่ยวข้องกับโครงการ ให้เลือกลิงค์ในฟิลด์ **รหัสโครงการ** บนแท็บ **ทั่วไป** บน FastTab **รายละเอียดของรายการ** ในมุมมองรายละเอียดของหน้า **ใบสั่งงานทั้งหมด** ในโมดูล **การจัดการสินทรัพย์** (**การจัดการสินทรัพย์** > **ทั่วไป** > **ใบสั่งงาน** > **ใบสั่งานทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="84ac6-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![รูปที่ 6](media/29-work-orders.png)

7. <span data-ttu-id="84ac6-123">ถ้าต้องการดูภาพรวมของโครงการที่เชื่อมโยงกับสินทรัพย์ถาวร ให้เลือก **สินทรัพย์ถาวร** > **สินทรัพย์ถาวร** > **สินทรัพย์ถาวร** แล้วจากนั้น ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกลิงค์สำหรับสินทรัพย์ถาวรที่จะเปิดมุมมองรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="84ac6-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="84ac6-124">ขยายบานหน้าต่าง **ข้อมูลที่เกี่ยวข้อง** ทางด้านขวาของหน้า และเลือก FastTab **โครงการที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="84ac6-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]