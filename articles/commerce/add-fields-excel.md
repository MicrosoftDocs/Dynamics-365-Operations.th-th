---
title: เพิ่มฟิลด์ลงในเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก
description: หัวข้อนี้จะอธิบายวิธีการเพิ่มฟิลด์ลงในเวิร์กบุ๊ก Microsoft Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกใน Microsoft Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: fb0435a617585689a87caa76f80e9774182576cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206330"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="27f16-103">เพิ่มฟิลด์ลงในเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="27f16-103">Add fields to an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27f16-104">หัวข้อนี้จะอธิบายวิธีการเพิ่มฟิลด์ลงในเวิร์กบุ๊ก Microsoft Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="27f16-104">This topic describes how to add fields to a Microsoft Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27f16-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="27f16-105">Overview</span></span>

<span data-ttu-id="27f16-106">เมื่อคุณสร้างไฟล์ Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกได้ ไฟล์จะมีการกรอกข้อมูลฟิลด์ค่าเริ่มต้นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="27f16-106">When you generate an Excel file so that you can edit retail transactions, the file is filled with some default fields.</span></span> <span data-ttu-id="27f16-107">ถ้ามองไม่เห็นฟิลด์ที่ต้องอัปเดตตามค่าเริ่มต้นในไฟล์ Excel ที่สร้างขึ้น คุณสามารถเพิ่มได้</span><span class="sxs-lookup"><span data-stu-id="27f16-107">If a field that must be updated isn't visible by default in the generated Excel file, you can add it.</span></span>

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a><span data-ttu-id="27f16-108">เพิ่มฟิลด์ลงในเวิร์กชีตในเวิร์กบุ๊ก Excel</span><span class="sxs-lookup"><span data-stu-id="27f16-108">Add fields to a worksheet in an Excel workbook</span></span>

<span data-ttu-id="27f16-109">เมื่อต้องการเพิ่มฟิลด์ลงในเวิร์กบุ๊ก Excel เพื่อให้คุณสามารถแก้ไขธุรกรรมการขายปลีกได้ ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="27f16-109">To add fields to an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="27f16-110">ดาวน์โหลดและเปิดไฟล์ Excel จากหน้า **ใบแจ้งยอด** หน้า **ธุรกรรมการขายปลีก** หรือไทล์ **ความล้มเหลวในการตรวจสอบความถูกต้องของธุรกรรม** ในพื้นที่ทำงาน **การเงินของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="27f16-110">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="27f16-111">เลือก **ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="27f16-111">Select **Design**.</span></span>
1. <span data-ttu-id="27f16-112">เลือกสัญลักษณ์ดินสอสําหรับตารางที่ต้องการ จากนั้นในรายการของฟิลด์ที่มีอยู่ ให้ค้นหาและเลือกฟิลด์ที่คุณต้องการเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="27f16-112">Select the pencil symbol for the desired table, and then, in the list of available fields, find and select the field that you want to add.</span></span>
1. <span data-ttu-id="27f16-113">เลือก **เพิ่ม** แล้วเลือก **อัปเดต**</span><span class="sxs-lookup"><span data-stu-id="27f16-113">Select **Add**, and then select **Update**.</span></span> <span data-ttu-id="27f16-114">คุณสามารถจัดลําดับฟิลด์ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="27f16-114">You can reorder fields.</span></span>
1. <span data-ttu-id="27f16-115">หลังจากการอัปเดตเสร็จสมบูรณ์ ให้เลือก **รีเฟรช** เพื่อดึงข้อมูลสําหรับคอลัมน์ใหม่</span><span class="sxs-lookup"><span data-stu-id="27f16-115">After the update is completed, select **Refresh** to fetch the data for the new column.</span></span>

<span data-ttu-id="27f16-116">ฟิลด์ใหม่และข้อมูลสําหรับฟิลด์นี้ควรจะสามารถใช้งานสําหรับการแก้ไขใน Excel ได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="27f16-116">The new field and data for it should now be available for editing in Excel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27f16-117">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="27f16-117">Additional resources</span></span>

[<span data-ttu-id="27f16-118">แก้ไขและตรวจสอบธุรกรรมเงินสดและการขนส่งและการจัดการเงินสด</span><span class="sxs-lookup"><span data-stu-id="27f16-118">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="27f16-119">แก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="27f16-119">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="27f16-120">แก้ไขมิติทางการเงินสำหรับธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="27f16-120">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="27f16-121">สร้างเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="27f16-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]