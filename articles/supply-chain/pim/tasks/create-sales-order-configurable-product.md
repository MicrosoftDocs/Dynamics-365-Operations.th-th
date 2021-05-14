---
title: สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้
description: 'กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921300"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="3113f-103">สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="3113f-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3113f-104">กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="3113f-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="3113f-105">ตัวอย่างนี้ใช้แบบจำลองลำโพง D0006 ในบริษัทข้อมูลสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="3113f-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="3113f-106">โดยทั่วไป ตัวประมวลผลใบสั่งขายจะใช้กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="3113f-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="3113f-107">สร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="3113f-107">Create a sales order</span></span>

1. <span data-ttu-id="3113f-108">ไปที่ **การขายและการตลาด \> พื้นที่ทำงาน \> การประมวลผลและการสอบถามใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="3113f-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="3113f-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3113f-109">Select **New**.</span></span>
1. <span data-ttu-id="3113f-110">เลือก **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="3113f-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="3113f-111">ในฟิลด์ **บัญชีลูกค้า** เลือก *US-001*</span><span class="sxs-lookup"><span data-stu-id="3113f-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="3113f-112">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3113f-112">Select **OK**.</span></span>
1. <span data-ttu-id="3113f-113">ในฟิลด์ **หมายเลขสินค้า** ให้เลือก *D0006*</span><span class="sxs-lookup"><span data-stu-id="3113f-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="3113f-114">สำหรับงานนี้ คุณต้องเลือกผลิตภัณฑ์ที่จัดโครงแบบได้</span><span class="sxs-lookup"><span data-stu-id="3113f-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="3113f-115">เลือก **ผลิตภัณฑ์และการจัดหาวัสดุ**</span><span class="sxs-lookup"><span data-stu-id="3113f-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="3113f-116">เลือก **ตั้งค่าคอนฟิกรายการ**</span><span class="sxs-lookup"><span data-stu-id="3113f-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="3113f-117">โปรดทราบว่ามีการเปลี่ยนแปลงราคาตามการตั้งค่าคอนฟิกที่ถูกเลือก และที่ฟิลด์ **รวมเคเบิล** ขณะนี้ถูกตั้งค่าเป็น *จริง*</span><span class="sxs-lookup"><span data-stu-id="3113f-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="3113f-118">สังเกตดูราคาและการตั้งค่าเริ่มต้นที่เลือกสำหรับเคเบิลดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="3113f-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="3113f-119">เลือก **โหลดเท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="3113f-119">Select **Load template**.</span></span>
    * <span data-ttu-id="3113f-120">ตัวอย่างนี้แสดงวิธีที่คุณสามารถใช้เท็มเพลตเพื่อเลือกการจัดโครงแบบที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="3113f-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="3113f-121">ถ้าคุณกำลังใช้กระบวนงานนี้เป็นคู่มืองาน และต้องการดูค่าแอททริบิวต์อื่นๆ ที่มีอยู่ คุณต้องเลือกปุ่ม **ปลดล็อค**</span><span class="sxs-lookup"><span data-stu-id="3113f-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="3113f-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3113f-122">Select **OK**.</span></span>
1. <span data-ttu-id="3113f-123">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3113f-123">Select **OK**.</span></span>
1. <span data-ttu-id="3113f-124">ขยายส่วน **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="3113f-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="3113f-125">เลือกแท็บ **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="3113f-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="3113f-126">ขณะนี้มีการแสดงรายการการจัดโครงแบบของสินค้าภายใต้มิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3113f-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="3113f-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3113f-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]