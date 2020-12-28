---
title: ภาพรวมของการจัดการวงจรการใช้งานใบสั่งผลิต
description: เมื่อมีการสร้างใบสั่งผลิต คำขอจะถูกเริ่มต้นเพื่อเริ่มการผลิตสินค้า ใบสั่งผลิตประกอบด้วยข้อมูลเกี่ยวกับสิ่งที่จะมีการผลิต ปริมาณที่จะผลิต และวันที่เสร็จสิ้นที่วางแผนไว้ ทั้งยังประกอบด้วยข้อมูลเกี่ยวกับวัสดุที่จะใช้ และกระบวนการที่จะดำเนินการตามเพื่อผลิตสินค้า
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80031737ab0d0c4ab1e4dbd5646ad91f1a010cd5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438628"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="d5292-105">ภาพรวมของการจัดการวงจรการใช้งานใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="d5292-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5292-106">เมื่อมีการสร้างใบสั่งผลิต คำขอจะถูกเริ่มต้นเพื่อเริ่มการผลิตสินค้า</span><span class="sxs-lookup"><span data-stu-id="d5292-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="d5292-107">ใบสั่งผลิตประกอบด้วยข้อมูลเกี่ยวกับสิ่งที่จะมีการผลิต ปริมาณที่จะผลิต และวันที่เสร็จสิ้นที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="d5292-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="d5292-108">ทั้งยังประกอบด้วยข้อมูลเกี่ยวกับวัสดุที่จะใช้ และกระบวนการที่จะดำเนินการตามเพื่อผลิตสินค้า</span><span class="sxs-lookup"><span data-stu-id="d5292-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="d5292-109">ใบสั่งผลิตผ่านไปยังขั้นตอนต่างๆของวงจรชีวิตของการผลิต </span><span class="sxs-lookup"><span data-stu-id="d5292-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="d5292-110">เมื่อสร้างใบสั่ง จะมีกำหนดสถานะ **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="d5292-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="d5292-111">เมื่อใบสั่งเสร็จสิ้นแล้ว จะมีกำหนดสถานะ **สิ้นสุด**</span><span class="sxs-lookup"><span data-stu-id="d5292-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="d5292-112">การตั้งค่าพารามิเตอร์ในแต่ละขั้นตอนอนุญาตให้ผู้ใช้สามารถตั้งค่าคอนฟิกในแต่ละขั้นตอนได้</span><span class="sxs-lookup"><span data-stu-id="d5292-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="d5292-113">การตั้งค่าสามารถถูกตั้งค่าสำหรับผู้ใช้คนเดียว หรือ สำหรับผู้ใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d5292-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="d5292-114">สูตรการผลิตและกระบวนการผลิตเป็นเอนทิตีหลักของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="d5292-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="d5292-115">พวกเขาจะถูกคัดลอกไปยังใบสั่งผลิตที่ขึ้นอยู่กับสินค้าที่เลือกและปริมาณที่กำลังจะผลิต</span><span class="sxs-lookup"><span data-stu-id="d5292-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="d5292-116">ก่อนที่จะเริ่มใบสั่งผลิต สามารถแก้ไขสูตรการผลิตและกระบวนการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="d5292-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="d5292-117">สามารถสร้างใบสั่งผลิตในสถานการณ์จำลองต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d5292-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="d5292-118">สร้างโดยการดำเนินการการวางแผนหลักตามความต้องการวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="d5292-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="d5292-119">สร้างขึ้นโดยตรงจากรายการใบสั่งขายหรือเมื่อมีการสร้างใบสั่งผลิตที่สูงกว่าและประเมิน (การจัดหาวัสดุที่มีการเชื่อมโยงความต้องการกับการจัดซื้อ)</span><span class="sxs-lookup"><span data-stu-id="d5292-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="d5292-120">สร้างด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d5292-120">Created manually.</span></span>




