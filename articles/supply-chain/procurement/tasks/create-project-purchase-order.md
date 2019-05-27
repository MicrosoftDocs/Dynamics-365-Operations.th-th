---
title: สร้างใบสั่งซื้อของโครงการ
description: กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อโครงการ
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0fa5f60abafb1200a61e1c9d8013fb9e28e28f48
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559173"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="faca1-103">สร้างใบสั่งซื้อของโครงการ</span><span class="sxs-lookup"><span data-stu-id="faca1-103">Create project purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="faca1-104">กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อโครงการ</span><span class="sxs-lookup"><span data-stu-id="faca1-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="faca1-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="faca1-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="faca1-106">ไปที่การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="faca1-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="faca1-107">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="faca1-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="faca1-108">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="faca1-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="faca1-109">คลิกงานของสินค้า</span><span class="sxs-lookup"><span data-stu-id="faca1-109">Click Item task.</span></span>
5. <span data-ttu-id="faca1-110">คลิกใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="faca1-110">Click Purchase order.</span></span>
6. <span data-ttu-id="faca1-111">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="faca1-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="faca1-112">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="faca1-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="faca1-113">ขั้นตอนเหล่านี้ไม่จำเป็น แต่จะทำให้ใบสั่งซื้อง่ายขึ้นโดยการตั้งค่าไซต์เริ่มต้นและคลังสินค้าสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="faca1-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="faca1-114">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="faca1-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="faca1-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="faca1-115">Click OK.</span></span>
10. <span data-ttu-id="faca1-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="faca1-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="faca1-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="faca1-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="faca1-118">ซึ่งอาจเป็นหมายเลขสินค้าหรือประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="faca1-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="faca1-119">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="faca1-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="faca1-120">คลิกแท็บโครงการ</span><span class="sxs-lookup"><span data-stu-id="faca1-120">Click the Project tab.</span></span>
    * <span data-ttu-id="faca1-121">ตรวจสอบว่าราคาขายและราคาต้นทุนพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="faca1-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="faca1-122">ถ้าไม่พร้อมใช้งาน แต่จำเป็นต้องใช้ ให้ป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="faca1-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="faca1-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="faca1-123">Click Save.</span></span>

