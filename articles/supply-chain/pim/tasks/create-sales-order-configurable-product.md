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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9a9b60fbcf6de5377b44ca03d4ffc792a6a78f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207002"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="2ce83-103">สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="2ce83-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ce83-104">กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="2ce83-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="2ce83-105">ตัวอย่างนี้ใช้แบบจำลองลำโพง D0006 ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="2ce83-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="2ce83-106">โดยทั่วไป ตัวประมวลผลใบสั่งขายจะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="2ce83-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="2ce83-107">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="2ce83-107">Create a sales order</span></span>
1. <span data-ttu-id="2ce83-108">คลิกที่การประมวลผลและการสอบถามใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="2ce83-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="2ce83-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2ce83-109">Click New.</span></span>
3. <span data-ttu-id="2ce83-110">คลิกที่ใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="2ce83-110">Click Sales order.</span></span>
4. <span data-ttu-id="2ce83-111">ในฟิลด์บัญชีลูกค้า เลือก US-001</span><span class="sxs-lookup"><span data-stu-id="2ce83-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="2ce83-112">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2ce83-112">Click OK.</span></span>
6. <span data-ttu-id="2ce83-113">ในฟิลด์หมายเลขสินค้า ให้เลือก D0006</span><span class="sxs-lookup"><span data-stu-id="2ce83-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="2ce83-114">สำหรับงานนี้ คุณต้องเลือกผลิตภัณฑ์ที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="2ce83-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="2ce83-115">คลิกที่ผลิตภัณฑ์และการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="2ce83-115">Click Product and supply.</span></span>
8. <span data-ttu-id="2ce83-116">คลิกตั้งค่าคอนฟิกรายการ</span><span class="sxs-lookup"><span data-stu-id="2ce83-116">Click Configure line.</span></span>
    * <span data-ttu-id="2ce83-117">โปรดทราบว่ามีการเปลี่ยนแปลงราคาตามการจัดโครงแบบที่เลือก และขณะนี้ฟิลด์รวมเคเบิลถูกตั้งค่าเป็น จริง</span><span class="sxs-lookup"><span data-stu-id="2ce83-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="2ce83-118">สังเกตดูราคาและการตั้งค่าเริ่มต้นที่เลือกสำหรับเคเบิลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="2ce83-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="2ce83-119">คลิกโหลดเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2ce83-119">Click Load template.</span></span>
    * <span data-ttu-id="2ce83-120">ตัวอย่างนี้แสดงวิธีที่คุณสามารถใช้เท็มเพลตเพื่อเลือกการจัดโครงแบบที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="2ce83-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="2ce83-121">ถ้าคุณกำลังใช้กระบวนงานนี้เป็นคู่มืองาน และต้องการดูค่าแอททริบิวต์อื่นๆ ที่มีอยู่ คุณจะต้องคลิกปุ่ม ปลดล็อค</span><span class="sxs-lookup"><span data-stu-id="2ce83-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="2ce83-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2ce83-122">Click OK.</span></span>
11. <span data-ttu-id="2ce83-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2ce83-123">Click OK.</span></span>
12. <span data-ttu-id="2ce83-124">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="2ce83-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="2ce83-125">คลิกแท็บผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2ce83-125">Click the Product tab.</span></span>
    * <span data-ttu-id="2ce83-126">ขณะนี้มีการแสดงรายการการจัดโครงแบบของสินค้าภายใต้มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2ce83-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="2ce83-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2ce83-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="2ce83-128">เลือกการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2ce83-128">Select the product configuration</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]