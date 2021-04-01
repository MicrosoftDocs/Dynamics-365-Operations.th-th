---
title: สร้างใบสั่งซื้อของโครงการ
description: กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อโครงการ
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, PurchTablePart, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1eef6f4e0ef4b0c33572156b702c182456e3360d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237238"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="d274a-103">สร้างใบสั่งซื้อของโครงการ</span><span class="sxs-lookup"><span data-stu-id="d274a-103">Create project purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d274a-104">กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อโครงการ</span><span class="sxs-lookup"><span data-stu-id="d274a-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="d274a-105">งานนี้ใช้ชุดข้อมูล USSI</span><span class="sxs-lookup"><span data-stu-id="d274a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d274a-106">ไปที่การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d274a-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="d274a-107">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d274a-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="d274a-108">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="d274a-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="d274a-109">คลิกงานของสินค้า</span><span class="sxs-lookup"><span data-stu-id="d274a-109">Click Item task.</span></span>
5. <span data-ttu-id="d274a-110">คลิกใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="d274a-110">Click Purchase order.</span></span>
6. <span data-ttu-id="d274a-111">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d274a-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="d274a-112">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d274a-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d274a-113">ขั้นตอนเหล่านี้ไม่จำเป็น แต่จะทำให้ใบสั่งซื้อง่ายขึ้นโดยการตั้งค่าไซต์เริ่มต้นและคลังสินค้าสำหรับบรรทัดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="d274a-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="d274a-114">ในฟิลด์คลังสินค้า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d274a-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="d274a-115">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d274a-115">Click OK.</span></span>
10. <span data-ttu-id="d274a-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d274a-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="d274a-117">ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d274a-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="d274a-118">ซึ่งอาจเป็นหมายเลขสินค้าหรือประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="d274a-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="d274a-119">ขยายส่วน รายละเอียดของรายการ</span><span class="sxs-lookup"><span data-stu-id="d274a-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="d274a-120">คลิกแท็บโครงการ</span><span class="sxs-lookup"><span data-stu-id="d274a-120">Click the Project tab.</span></span>
    * <span data-ttu-id="d274a-121">ตรวจสอบว่าราคาขายและราคาต้นทุนพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d274a-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="d274a-122">ถ้าไม่พร้อมใช้งาน แต่จำเป็นต้องใช้ ให้ป้อนข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d274a-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="d274a-123">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d274a-123">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]