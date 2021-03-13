---
title: สร้างโครงการตัวรวมข้อมูล (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างโครงการตัวรวมข้อมูล
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009467"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="ef80f-103">สร้างโครงการตัวรวมข้อมูล (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="ef80f-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ef80f-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างโครงการตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="ef80f-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="ef80f-105">ลงชื่อเข้าใช้ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ef80f-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="ef80f-106">ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือก **เอนทิตีข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ef80f-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="ef80f-107">รอจนกว่าจะมีการรีเฟรชเอนทิตีข้อมูลทั้งหมดก่อนที่คุณจะไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="ef80f-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="ef80f-108">เปิด [พอร์ทัล Power Apps](https://make.powerapps.com/) และปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ef80f-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="ef80f-109">ให้เลือกสภาพแวดล้อมที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ef80f-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="ef80f-110">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ข้อมูล \> การเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="ef80f-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="ef80f-111">เชื่อมต่อกับอินสแตนซ์ที่เหมาะสมของรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ef80f-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="ef80f-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ef80f-112">Dynamics 365</span></span>
        - <span data-ttu-id="ef80f-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="ef80f-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="ef80f-114">เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ef80f-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="ef80f-115">เลือก **ตัวรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="ef80f-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="ef80f-116">เลือก **การตั้งค่าการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="ef80f-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="ef80f-117">เลือก **การตั้งค่าการเชื่อมต่อใหม่**</span><span class="sxs-lookup"><span data-stu-id="ef80f-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="ef80f-118">ป้อนชื่อสำหรับการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="ef80f-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="ef80f-119">เลือกการเชื่อมต่อที่ถูกต้องสำหรับสินค้าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ef80f-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="ef80f-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ef80f-120">Dynamics 365</span></span>
        - <span data-ttu-id="ef80f-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="ef80f-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="ef80f-122">เลือกการแม็ปองค์กรที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="ef80f-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="ef80f-123">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ef80f-123">Select **Create**.</span></span>

5. <span data-ttu-id="ef80f-124">เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ef80f-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="ef80f-125">สร้างโครงการการรวมข้อมูลสำหรัแม่แบบต่อไปนี้โดยใช้การตั้งค่าการเชื่อมต่อที่คุณเพิ่งสร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="ef80f-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="ef80f-126">ผลลัพธ์เชิงลึกของการชำระเงินของลูกค้า (CD to Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="ef80f-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="ef80f-127">ผลลัพธ์ของชุดเวลาของกระแสเงินสด (CD to Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="ef80f-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="ef80f-128">ผลลัพธ์ของชุดเวลาของงบประมาณ (CD to Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="ef80f-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="ef80f-129">ตั้งค่าการจัดกำหนดการที่เหมาะสมสำหรับแต่ละโครงการ</span><span class="sxs-lookup"><span data-stu-id="ef80f-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="ef80f-130">ถ้าคุณไม่เห็นเอนทิตีที่จำเป็นใน CDS โปรดไปที่ **เครดิตและการเรียกเก็บเงิน > การตั้งค่า > ข้อมูลเชิงลึกทางการเงิน > พารามิเตอร์ข้อมูลเชิงลึกของการเงิน** ให้เปิดใช้งานลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าและคลิกที่ปุ่ม **สร้างแบบจำลองการคาดคะเน**</span><span class="sxs-lookup"><span data-stu-id="ef80f-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="ef80f-131">เมื่อการใช้งานของโมเดล AI เสร็จสมบูรณ์ (ประสบความสำเร็จหรือล้มเหลว) เอนทิตี CDS ที่จำเป็นในการสร้างการรวมจะถูกปรับใช้ใน CDS</span><span class="sxs-lookup"><span data-stu-id="ef80f-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="ef80f-132">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="ef80f-132">Privacy notice</span></span>

<span data-ttu-id="ef80f-133">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="ef80f-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
