---
title: การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่อนุญาตให้คุณรันรายงานการแยกสินค้าคงคลัง และทำให้ผลลัพธ์พร้อมใช้งานเป็นฟอร์มและแผนภูมิ
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: c4a1480cf96a4ba753b436c04eb8f7b01379da48
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759675"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="336e8-103">การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="336e8-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="336e8-104">ใน Microsoft Dynamics 365 Supply Chain Management คุณสามารถรันรายงาน **การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง** และทำให้ผลลัพธ์พร้อมใช้งานเป็นฟอร์มและแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="336e8-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="336e8-105">ในฟอร์ม คอลัมน์ และยอดดุลรวมจะมีการปรับปรุงแบบไดนามิก ทั้งนี้ขึ้นอยู่กับโครงร่างที่มีการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="336e8-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="336e8-106">แผนภูมิแสดงภาพรวมทางการแสดงผล ซึ่งสนับสนุนการกรองข้อมูลและช่วยให้คุณสามารถดูรายละเอียดแนวลึกได้</span><span class="sxs-lookup"><span data-stu-id="336e8-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="336e8-107">นอกจากนี้ เอนทิตี้ข้อมูลที่ชื่อ **รายงานอายุหนี้ของสินค้าคงคลัง** ช่วยให้คุณสามารถส่งออกผลลัพธ์ของรายงาน **การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง** เพื่อให้มีการรันกับรูปแบบ เช่น ไฟล์ Microsoft Excel หรือไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="336e8-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="336e8-108">วิธีการรันรายงาน **การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง** นี้มีประโยชน์ ในกรณีที่ผลลัพธ์มีหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="336e8-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="336e8-109">ตัวอย่างเช่น ผลลัพธ์จะประกอบด้วยบรรทัดจำนวนมาก ถ้าคุณมีสินค้า 50,000 รายการ และร้านค้า 300 ร้านที่สร้างขึ้นเป็นคลังสินค้า และคุณร้องขอการแยกอายุสินค้าคงคลังโดยเรียงตามสินค้า ไซต์ และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="336e8-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="336e8-110">เปิดใช้งานคุณลักษณะรายงานการจัดเก็บมูลค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="336e8-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="336e8-111">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="336e8-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="336e8-112">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งานได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="336e8-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="336e8-113">ต่อไปนี้มีการแสดงรายการคุณลักษณะเป็น:</span><span class="sxs-lookup"><span data-stu-id="336e8-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="336e8-114">**โมดูล** - การจัดการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="336e8-114">**Module** - Cost management</span></span>
- <span data-ttu-id="336e8-115">**ชื่อคุณลักษณะ** - การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="336e8-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="336e8-116">รันการจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="336e8-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="336e8-117">ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> ที่เก็บข้อมูลรายงานการแยกอายุสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="336e8-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="336e8-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="336e8-118">Select **New**.</span></span>
1. <span data-ttu-id="336e8-119">ในฟิลด์ **รหัสกระบวนการ – ชื่อ** ป้อนชื่อเฉพาะสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="336e8-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="336e8-120">เลือกรายงาน **รหัสประจำตัว - รหัส** และกรองข้อมูลตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="336e8-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="336e8-121">การดำเนินการรายงานจะทำในชุดงานเสมอ</span><span class="sxs-lookup"><span data-stu-id="336e8-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="336e8-122">หลังจากชุดงานเสร็จสมบูรณ์ ผลลัพธ์จะแสดงขึ้นบนเพจ **ที่เก็บข้อมูลรายงานการแยกอายุสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="336e8-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="336e8-123">เมื่อต้องการดูผลลัพธ์เป็นฟอร์มที่มีโครงร่างกริดแบบดั้งเดิม ให้เลือก **ดูรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="336e8-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="336e8-124">เมื่อต้องการดูผลลัพธ์เป็นแผนภูมิรวม ให้เลือก **ดูแผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="336e8-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="336e8-125">ฟอร์มจะไม่มีผลรวมย่อยที่กำหนดไว้ในโครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="336e8-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="336e8-126">เอนทิตี้ข้อมูล **รายงานอายุหนี้ของสินค้าคงคลัง** ช่วยให้คุณสามารถส่งออกผลลัพธ์ของรายงาน **การจัดเก็บรายงานอายุหนี้ของสินค้าคงคลัง** ได้โดยการใช้ตัวกรองสำหรับฟิลด์ **รหัสกระบวนการ - ชื่อ** ไปยังรูปแบบใดๆ ที่การจัดการข้อมูลสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="336e8-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
