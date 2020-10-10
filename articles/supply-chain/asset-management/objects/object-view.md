---
title: มุมมองสินทรัพย์
description: หัวข้อนี้อธิบายมุมมองสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc4cd9ada9c1f64b434cd657eb5f5654c1328ef4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888773"
---
# <a name="asset-view"></a><span data-ttu-id="be84a-103">มุมมองสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="be84a-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="be84a-104">หัวข้อนี้อธิบายมุมมองสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="be84a-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="be84a-105">หน้า **มุมมองสินทรัพย์** แสดงสินทรัพย์ที่ใช้งานอยู่ และตำแหน่งที่ทำงานในมุมมองแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="be84a-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="be84a-106">ดังนั้น คุณสามารถดูภาพรวมของความสัมพันธ์ของสินทรัพย์กับตำแหน่งที่ทำงานได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="be84a-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="be84a-107">นอกจากนี้ คุณสามารถดูข้อมูลโดยละเอียดเกี่ยวกับตำแหน่งที่ทำงาน สินทรัพย์ และสูตรการผลิตที่เกี่ยวข้อง (BOMs)</span><span class="sxs-lookup"><span data-stu-id="be84a-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="be84a-108">นอกจากนี้ คุณยังสามารถดูภาพรวมด่วนของคำขอการบำรุงรักษาที่ใช้งานอยู่ และใบสั่งงานที่เกี่ยวข้องกับสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="be84a-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="be84a-109">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **มุมมองสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="be84a-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="be84a-110">เมื่อต้องการเปลี่ยนมุมมองที่แสดงบนหน้า ให้เลือกค่าใหม่ในฟิลด์ **มุมมอง**</span><span class="sxs-lookup"><span data-stu-id="be84a-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="be84a-111">มุมมองเริ่มต้นที่จะแสดงเมื่อคุณเปิดหน้า **มุมมองสินทรัพย์** ขึ้นอยู่กับค่าที่เลือกในฟิลด์ **มุมมอง** บนแท็บ **สินทรัพย์** ของหน้า **พารามิเตอร์การจัดการสินทรัพย์** (**การจัดการสินทรัพย์** \> **การตั้งค่า** \> **พารามิเตอร์การจัดการสินทรัพย์**)</span><span class="sxs-lookup"><span data-stu-id="be84a-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="be84a-112">ที่ด้านขวาของหน้า FastTab จะแสดงรายละเอียดของมุมมองที่เลือก</span><span class="sxs-lookup"><span data-stu-id="be84a-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="be84a-113">บันทึกการแสดงเส้นทางที่ปรากฏเหนือมุมมองแผนภูมิจะแสดงการเลือกปัจจุบันในมุมมองแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="be84a-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="be84a-114">บันทึกการแสดงเส้นทางนี้ใช้รูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="be84a-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="be84a-115">รหัสตำแหน่งที่ทำงาน / รหัสตำแหน่งที่ทำงาน (ถ้ามีตำแหน่งที่ทำงานมากกว่าหนึ่งแห่ง) \> รหัสสินทรัพย์ / รหัสสินทรัพย์ (ถ้ามีสินทรัพย์มากกว่าหนึ่งรายการ) - หมายเลขสินค้า</span><span class="sxs-lookup"><span data-stu-id="be84a-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="be84a-116">ถ้าคุณได้เลือกสินทรัพย์ในมุมมองแผนภูมิ คุณสามารถเลือก **คำขอที่ใช้งานอยู่** หรือ **ใบสั่งงานที่ใช้งานอยู่** เพื่อดูคำขอการบำรุงรักษา หรือใบสั่งงานที่เกี่ยวข้องกับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="be84a-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="be84a-117">นอกจากนี้ คุณยังสามารถเลือก **เปิด** \> **ตำแหน่งที่ทำงาน** **สินทรัพย์** หรือ **BOM สินทรัพย์** เพื่อเปิดมุมมองที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="be84a-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="be84a-118">ตัวเลือก **ตำแหน่งที่ทำงานของสินทรัพย์** ที่คุณสามารถเลือกได้ในฟิลด์ **มุมมอง** ยังพร้อมใช้งานในการค้นหาสินทรัพย์ใดๆ ที่คุณสามารถเลือกสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="be84a-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="be84a-119">มุมมองแผนภูมิจะแสดงอยู่บนแท็บ **มุมมองสินทรัพย์** ตัวอย่างเช่น ตำแหน่งที่คุณ [สร้างสินทรัพย์](../objects/create-an-object.md) ให้สร้างคำขอการบำรุงรักษา หรือสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="be84a-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>
