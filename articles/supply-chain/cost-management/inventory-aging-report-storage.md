---
title: รายงานการแยกสินค้าคงคลัง
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่อนุญาตให้คุณรันรายงานการแยกสินค้าคงคลัง และทำให้ผลลัพธ์พร้อมใช้งานเป็นฟอร์มและแผนภูมิ
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
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
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201637"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="d9a14-103">รายงานการแยกสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9a14-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d9a14-104">ใน Microsoft Dynamics 365 Supply Chain Management คุณสามารถรันรายงาน **การแยกอายุสินค้าคงคลัง** และทำให้ผลลัพธ์พร้อมใช้งานเป็นฟอร์มและแผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="d9a14-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="d9a14-105">ในฟอร์ม คอลัมน์ และยอดดุลรวมจะมีการปรับปรุงแบบไดนามิก ทั้งนี้ขึ้นอยู่กับโครงร่างที่มีการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="d9a14-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="d9a14-106">แผนภูมิแสดงภาพรวมทางการแสดงผล ซึ่งสนับสนุนการกรองข้อมูลและช่วยให้คุณสามารถดูรายละเอียดแนวลึกได้</span><span class="sxs-lookup"><span data-stu-id="d9a14-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="d9a14-107">นอกจากนี้ เอนทิตี้ข้อมูลที่ชื่อ **รายงานการแยกอายุสินค้าคงคลัง** ช่วยให้คุณสามารถส่งออกผลลัพธ์ของรายงาน **การแยกอายุสินค้าคงคลัง** เพื่อให้มีการรันกับรูปแบบ เช่น ไฟล์ Microsoft Excel หรือไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="d9a14-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="d9a14-108">วิธีการรันรายงาน **การแยกอายุสินค้าคงคลัง** นี้มีประโยชน์ในกรณีที่ผลลัพธ์มีหลายบรรทัด</span><span class="sxs-lookup"><span data-stu-id="d9a14-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="d9a14-109">ตัวอย่างเช่น ผลลัพธ์จะประกอบด้วยบรรทัดจำนวนมาก ถ้าคุณมีสินค้า 50,000 รายการ และร้านค้า 300 ร้านที่สร้างขึ้นเป็นคลังสินค้า และคุณร้องขอการแยกอายุสินค้าคงคลังโดยเรียงตามสินค้า ไซต์ และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="d9a14-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="d9a14-110">รันรายงานการแยกอายุสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="d9a14-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="d9a14-111">ไปที่ **การจัดการต้นทุน \> การสอบถามและรายงาน \> ที่เก็บข้อมูลรายงานการแยกอายุสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="d9a14-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="d9a14-112">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d9a14-112">Select **New**.</span></span>
1. <span data-ttu-id="d9a14-113">ในฟิลด์ **รหัสกระบวนการ – ชื่อ** ป้อนชื่อเฉพาะสำหรับรายงาน</span><span class="sxs-lookup"><span data-stu-id="d9a14-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="d9a14-114">เลือกรายงาน **รหัสประจำตัว - รหัส** และกรองข้อมูลตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="d9a14-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="d9a14-115">การดำเนินการรายงานจะทำในชุดงานเสมอ</span><span class="sxs-lookup"><span data-stu-id="d9a14-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="d9a14-116">หลังจากชุดงานเสร็จสมบูรณ์ ผลลัพธ์จะแสดงขึ้นบนเพจ **ที่เก็บข้อมูลรายงานการแยกอายุสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="d9a14-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="d9a14-117">เมื่อต้องการดูผลลัพธ์เป็นฟอร์มที่มีโครงร่างกริดแบบดั้งเดิม ให้เลือก **ดูรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="d9a14-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="d9a14-118">เมื่อต้องการดูผลลัพธ์เป็นแผนภูมิรวม ให้เลือก **ดูแผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="d9a14-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9a14-119">ฟอร์มจะไม่มีผลรวมย่อยที่กำหนดไว้ในโครงร่างรายงาน</span><span class="sxs-lookup"><span data-stu-id="d9a14-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="d9a14-120">เอนทิตี้ข้อมูล **รายงานการแยกอายุสินค้าคงคลัง** ช่วยให้คุณสามารถส่งออกผลลัพธ์ของรายงานการ **การแยกอายุสินค้าคงคลัง** ได้โดยการใช้ตัวกรองข้อมูลสำหรับฟิลด์ **รหัสกระบวนการ - ชื่อ** ไปยังรูปแบบใดๆ ที่สนับสนุนการจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d9a14-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
