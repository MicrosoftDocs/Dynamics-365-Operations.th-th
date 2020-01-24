---
title: สลับการออกแบบของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีสลับการรวมข้อมูลของผู้จัดจำหน่ายระหว่างแอป Finance and Operations และ Common Data Service
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902736"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="9f1db-103">สลับการออกแบบของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9f1db-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="9f1db-104">โฟลว์ข้อมูลของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9f1db-104">Vendor data flow</span></span> 

<span data-ttu-id="9f1db-105">หากคุณใช้แอป Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการแยกข้อมูลผู้จัดจำหน่ายออกจากข้อมูลลูกค้า ใช้การออกแบบผู้จัดจำหน่ายพื้นฐานนี้</span><span class="sxs-lookup"><span data-stu-id="9f1db-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![ขั้นตอนของผู้จัดจำหน่ายพื้นฐาน](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="9f1db-107">ถ้าคุณใช้แอป Dynamics 365 อื่น สำหรับการพัฒนาความเชี่ยวชาญของผู้จัดจำหน่าย และคุณต้องการใช้เอนทิตี **บัญชี** ต่อเพื่อการเก็บข้อมูลผู้จัดจำหน่าย ใช้การออกแบบผู้จัดจำหน่ายแบบขยายนี้</span><span class="sxs-lookup"><span data-stu-id="9f1db-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="9f1db-108">ในการออกแบบนี้ข้อมูลของผู้จัดจำหน่ายแบบขยาย เช่นสถานะระงับของผู้จัดจำหน่ายและโพรไฟล์ผู้จัดจำหน่ายถูกจัดเก็บในเอนทิตี **ผู้จัดจำหน่าย** ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9f1db-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![โฟลว์ของผู้จัดจำหน่ายแบบขยาย](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="9f1db-110">ทำตามขั้นตอนด้านล่างเพื่อใช้การออกแบบผู้จัดจำหน่ายแบบขยาย:</span><span class="sxs-lookup"><span data-stu-id="9f1db-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="9f1db-111">แพคเกจโซลูชัน **SupplyChainCommon** ประกอบด้วยเท็มเพลตการประมวลผลลำดับงาน ดังที่แสดงในรูปแบบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9f1db-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9f1db-112">![เท็มเพลตการประมวลผลลำดับงาน](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="9f1db-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="9f1db-113">สร้างกระบวนการลำดับงานใหม่โดยใช้เท็มเพลตการประมวลผลลำดับงาน:</span><span class="sxs-lookup"><span data-stu-id="9f1db-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="9f1db-114">สร้างกระบวนการลำดับงานใหม่สำหรับเอนทิตี **ผู้จัดจำหน่าย** โดยใช้เท็มเพลตการประมวลผลลำดับงาน **สร้างผู้จัดจำหน่ายในเอนทิตีบัญชี** และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9f1db-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9f1db-115">ลำดับงานนี้จะจัดการสถานการณ์จำลองการสร้างผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="9f1db-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f1db-116">![สร้างผู้จัดจำหน่ายในเอนทิตี้บัญชี](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="9f1db-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="9f1db-117">สร้างกระบวนการลำดับงานใหม่สำหรับเอนทิตี **ผู้จัดจำหน่าย** โดยใช้เท็มเพลตการประมวลผลลำดับงาน **อัปเดตเอนทิตีบัญชี** และคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9f1db-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9f1db-118">ลำดับงานนี้จะจัดการสถานการณ์จำลองการอัปเดตผู้จัดจำหน่าย สำหรับเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="9f1db-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f1db-119">![อัพเดตเอนทิตีบัญชี](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="9f1db-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="9f1db-120">สร้างกระบวนการลำดับงานใหม่จากเท็มเพลตที่สร้างบนเอนทิตี **บัญชี**</span><span class="sxs-lookup"><span data-stu-id="9f1db-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f1db-121">![สร้างผู้จัดจำหน่ายในเอนทิตีผู้จัดจำหน่าย](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="9f1db-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="9f1db-122">![อัพเดตเอนทิตีผู้จัดจำหน่าย](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="9f1db-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="9f1db-123">คุณสามารถตั้งค่าคอนฟิกลำดับงานเป็นลำดับงานแบบเรียลไทม์หรือแบ็คกราวน์ตามความต้องการของคุณ</span><span class="sxs-lookup"><span data-stu-id="9f1db-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f1db-124">![การแปลงเป็นลำดับงานพื้นหลัง](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="9f1db-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="9f1db-125">เปิดใช้ลำดับงานที่คุณสร้างขึ้นในเอนทิตี **บัญชี** และ **ผู้จัดจำหน่าย** เพื่อเริ่มต้นใช้งานเอนทิตี **บัญชี** สำหรับการจัดเก็บข้อมูลผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9f1db-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
