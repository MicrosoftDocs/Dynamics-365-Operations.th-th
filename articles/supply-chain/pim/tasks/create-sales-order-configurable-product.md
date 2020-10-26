---
title: สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้
description: 'กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 988d87757019d20dcaf675af925166ed376685f5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985496"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="898e4-103">สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="898e4-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="898e4-104">กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="898e4-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="898e4-105">ตัวอย่างนี้ใช้แบบจำลองลำโพง D0006 ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="898e4-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="898e4-106">โดยทั่วไป ตัวประมวลผลใบสั่งขายจะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="898e4-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="898e4-107">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="898e4-107">Create a sales order</span></span>
1. <span data-ttu-id="898e4-108">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="898e4-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="898e4-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="898e4-109">Click New.</span></span>
3. <span data-ttu-id="898e4-110">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="898e4-110">Click Sales order.</span></span>
4. <span data-ttu-id="898e4-111">ในฟิลด์บัญชีลูกค้า เลือก US-001</span><span class="sxs-lookup"><span data-stu-id="898e4-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="898e4-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="898e4-112">Click OK.</span></span>
6. <span data-ttu-id="898e4-113">ในฟิลด์หมายเลขสินค้า ให้เลือก D0006</span><span class="sxs-lookup"><span data-stu-id="898e4-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="898e4-114">สำหรับงานนี้ คุณต้องเลือกผลิตภัณฑ์ที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="898e4-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="898e4-115">คลิกที่ผลิตภัณฑ์และการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="898e4-115">Click Product and supply.</span></span>
8. <span data-ttu-id="898e4-116">คลิกตั้งค่าคอนฟิกรายการ</span><span class="sxs-lookup"><span data-stu-id="898e4-116">Click Configure line.</span></span>
    * <span data-ttu-id="898e4-117">โปรดทราบว่ามีการเปลี่ยนแปลงราคาตามการจัดโครงแบบที่เลือก และขณะนี้ฟิลด์รวมเคเบิลถูกตั้งค่าเป็น จริง</span><span class="sxs-lookup"><span data-stu-id="898e4-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="898e4-118">สังเกตดูราคาและการตั้งค่าเริ่มต้นที่เลือกสำหรับเคเบิลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="898e4-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="898e4-119">คลิกโหลดเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="898e4-119">Click Load template.</span></span>
    * <span data-ttu-id="898e4-120">ตัวอย่างนี้แสดงวิธีที่คุณสามารถใช้เท็มเพลตเพื่อเลือกการจัดโครงแบบที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="898e4-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="898e4-121">ถ้าคุณกำลังใช้กระบวนงานนี้เป็นคู่มืองาน และต้องการดูค่าแอททริบิวต์อื่นๆ ที่มีอยู่ คุณจะต้องคลิกปุ่ม ปลดล็อค</span><span class="sxs-lookup"><span data-stu-id="898e4-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="898e4-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="898e4-122">Click OK.</span></span>
11. <span data-ttu-id="898e4-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="898e4-123">Click OK.</span></span>
12. <span data-ttu-id="898e4-124">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="898e4-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="898e4-125">คลิกแท็บผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="898e4-125">Click the Product tab.</span></span>
    * <span data-ttu-id="898e4-126">ขณะนี้มีการแสดงรายการการจัดโครงแบบของสินค้าภายใต้มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="898e4-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="898e4-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="898e4-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="898e4-128">เลือกการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="898e4-128">Select the product configuration</span></span>

