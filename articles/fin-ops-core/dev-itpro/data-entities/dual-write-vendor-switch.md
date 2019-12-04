---
title: สลับระหว่างการออกแบบผู้จัดจำหน่าย
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772375"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="9e439-102">สลับระหว่างการออกแบบผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9e439-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="9e439-103">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9e439-103">Vendor data flow</span></span> 

<span data-ttu-id="9e439-104">หากคุณใช้แอป Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการแยกข้อมูลผู้จัดจำหน่ายออกจากข้อมูลลูกค้า ใช้การออกแบบผู้จัดจำหน่ายพื้นฐานนี้</span><span class="sxs-lookup"><span data-stu-id="9e439-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![ขั้นตอนของผู้จัดจำหน่ายพื้นฐาน](media/dual-write-switch-1.png)
 
<span data-ttu-id="9e439-106">ถ้าคุณใช้แอป Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการใช้เอนทิตี **บัญชี** ต่อเพื่อการเก็บข้อมูลผู้จัดจำหน่าย ใช้การออกแบบผู้จัดจำหน่ายแบบขยายนี้</span><span class="sxs-lookup"><span data-stu-id="9e439-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="9e439-107">ในการออกแบบนี้ข้อมูลของผู้จัดจำหน่ายแบบขยาย เช่นสถานะระงับของผู้จัดจำหน่ายและโพรไฟล์ผู้จัดจำหน่ายถูกจัดเก็บในเอนทิตี **ผู้จัดจำหน่าย** ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9e439-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![โฟลว์ของผู้จัดจำหน่ายแบบขยาย](media/dual-write-switch-2.png)
 
<span data-ttu-id="9e439-109">ทำตามขั้นตอนด้านล่างเพื่อใช้การออกแบบผู้จัดจำหน่ายแบบขยาย:</span><span class="sxs-lookup"><span data-stu-id="9e439-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="9e439-110">แพคเกจโซลูชัน **SupplyChainCommon** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงาน ดังที่แสดงในรูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9e439-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9e439-111">![เท็มเพลตการประมวลผลลำดับงาน](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="9e439-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="9e439-112">สร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน:</span><span class="sxs-lookup"><span data-stu-id="9e439-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="9e439-113">สร้างกระบวนการลำดับงานใหม่สำหรับเอนทิตี **ผู้จัดจำหน่าย** โดยใช้เท็มเพลตการประมวลผลลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตีบัญชี** และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9e439-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9e439-114">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="9e439-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e439-115">![สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="9e439-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="9e439-116">สร้างกระบวนการลำดับงานใหม่สำหรับเอนทิตี **ผู้จัดจำหน่าย** โดยใช้เท็มเพลตการประมวลผลลำดับงาน **อัปเดตเอนทิตีบัญชี** และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9e439-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9e439-117">ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="9e439-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e439-118">![อัพเดตเอนทิตีบัญชี](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="9e439-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="9e439-119">สร้างกระบวนการลำดับงานใหม่จากเท็มเพลตที่สร้างบนเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="9e439-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e439-120">![สร้างผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="9e439-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="9e439-121">![อัพเดตเอนทิตีผู้จัดจำหน่าย](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="9e439-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="9e439-122">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์หรือแบ็คกราวน์ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="9e439-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9e439-123">![การแปลงเป็นลำดับงานพื้นหลัง](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="9e439-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="9e439-124">เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี **บัญชี** ของ Customer Engagement สำหรับการจัดเก็บข้อมูลผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9e439-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
