---
title: สร้างโครงการตัวรวมข้อมูล (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างโครงการตัวรวมข้อมูล
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186479"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="fe696-103">สร้างโครงการตัวรวมข้อมูล (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="fe696-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fe696-104">หัวข้อนี้จะอธิบายถึงวิธีการสร้างโครงการตัวรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fe696-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="fe696-105">ลงชื่อเข้าใช้ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fe696-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="fe696-106">ให้ไปที่ **พื้นที่ทำงาน \> การจัดการข้อมูล** และเลือก **เอนทิตีข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fe696-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="fe696-107">รอจนกว่าจะมีการรีเฟรชเอนทิตีข้อมูลทั้งหมดก่อนที่คุณจะไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="fe696-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="fe696-108">เปิด [พอร์ทัล Power Apps](https://make.powerapps.com/) และปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fe696-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="fe696-109">ให้เลือกสภาพแวดล้อมที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="fe696-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="fe696-110">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ข้อมูล \> การเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="fe696-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="fe696-111">เชื่อมต่อกับอินสแตนซ์ที่เหมาะสมของรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fe696-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="fe696-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fe696-112">Dynamics 365</span></span>
        - <span data-ttu-id="fe696-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="fe696-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="fe696-114">เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fe696-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="fe696-115">เลือก **ตัวรวมข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="fe696-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="fe696-116">เลือก **การตั้งค่าการเชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="fe696-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="fe696-117">เลือก **การตั้งค่าการเชื่อมต่อใหม่**</span><span class="sxs-lookup"><span data-stu-id="fe696-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="fe696-118">ป้อนชื่อสำหรับการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="fe696-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="fe696-119">เลือกการเชื่อมต่อที่ถูกต้องสำหรับสินค้าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fe696-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="fe696-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="fe696-120">Dynamics 365</span></span>
        - <span data-ttu-id="fe696-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="fe696-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="fe696-122">เลือกการแม็ปองค์กรที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="fe696-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="fe696-123">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="fe696-123">Select **Create**.</span></span>

5. <span data-ttu-id="fe696-124">เปิด [สภาพแวดล้อม Power Apps](https://admin.powerapps.com/environments) และปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fe696-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="fe696-125">สร้างโครงการการรวมข้อมูลสำหรัแม่แบบต่อไปนี้โดยใช้การตั้งค่าการเชื่อมต่อที่คุณเพิ่งสร้างขึ้น:</span><span class="sxs-lookup"><span data-stu-id="fe696-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="fe696-126">ผลลัพธ์เชิงลึกของการชำระเงินของลูกค้า (CD to Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="fe696-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="fe696-127">ถ้าคุณใช้รุ่น 10.0.17 หรือใหม่กว่า คุณต้องใช้แม่แบบที่ชื่อ ผลลัพธ์เชิงลึกของการชำระเงินของลูกค้า (CD to Fin และ Ops 10.0.17+)</span><span class="sxs-lookup"><span data-stu-id="fe696-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="fe696-128">ผลลัพธ์ของชุดเวลาของกระแสเงินสด (CD to Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="fe696-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="fe696-129">ผลลัพธ์ของชุดเวลาของงบประมาณ (CD to Fin และ Ops)</span><span class="sxs-lookup"><span data-stu-id="fe696-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="fe696-130">ตั้งค่าการจัดกำหนดการที่เหมาะสมสำหรับแต่ละโครงการ</span><span class="sxs-lookup"><span data-stu-id="fe696-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="fe696-131">ถ้าคุณไม่เห็นเอนทิตีที่จำเป็นใน CDS โปรดไปที่ **เครดิตและการเรียกเก็บเงิน > การตั้งค่า > ข้อมูลเชิงลึกทางการเงิน > พารามิเตอร์ข้อมูลเชิงลึกของการเงิน** ให้เปิดใช้งานลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าและคลิกที่ปุ่ม **สร้างแบบจำลองการคาดคะเน**</span><span class="sxs-lookup"><span data-stu-id="fe696-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="fe696-132">เมื่อการใช้งานของโมเดล AI เสร็จสมบูรณ์ (ประสบความสำเร็จหรือล้มเหลว) เอนทิตี CDS ที่จำเป็นในการสร้างการรวมจะถูกปรับใช้ใน CDS</span><span class="sxs-lookup"><span data-stu-id="fe696-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
