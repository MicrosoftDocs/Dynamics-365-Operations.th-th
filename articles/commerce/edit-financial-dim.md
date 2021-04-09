---
title: แก้ไขมิติทางการเงินสำหรับธุรกรรมการขายปลีก
description: หัวข้อนี้อธิบายวิธีการแก้ไขมิติทางการเงินสําหรับธุรกรรมขายปลีกใน Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: ff16d8e2e75a877e5ca7de604c7915e908473da6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792716"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="eb891-103">แก้ไขมิติทางการเงินสำหรับธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="eb891-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb891-104">หัวข้อนี้อธิบายวิธีการแก้ไขมิติทางการเงินสําหรับธุรกรรมขายปลีกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="eb891-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="eb891-105">แก้ไขมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="eb891-105">Edit financial dimensions</span></span>

<span data-ttu-id="eb891-106">เมื่อต้องการแก้ไขมิติทางการเงินสําหรับธุรกรรมขายปลีกในศูนย์ควบคุม Commerce ให้ทําตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="eb891-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="eb891-107">เปิดหน้า **การตั้งค่าคอนฟิกมิติทางการเงินสำหรับการรวมแอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="eb891-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="eb891-108">เลือกเรกคอร์ด **การรวมมิติเริ่มต้น** ที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="eb891-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="eb891-109">บนแท็บด่วน **มิติทางการเงิน** ตรวจสอบให้แน่ใจว่ามิติทั้งหมดที่คุณต้องการแก้ไขในเวิร์กชีต Excel ที่มีอยู่ในรายการ **เลือกไว้**</span><span class="sxs-lookup"><span data-stu-id="eb891-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="eb891-110">สำหรับข้อมูลเพิ่มเติม ให้ดู [เอนทิตี้ข้อมูล](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities)</span><span class="sxs-lookup"><span data-stu-id="eb891-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="eb891-111">ดาวน์โหลดและเปิดไฟล์ Excel จากหน้า **ใบแจ้งยอด** หน้า **ธุรกรรมการขายปลีก** หรือไทล์ **ความล้มเหลวในการตรวจสอบความถูกต้องของธุรกรรม** ในพื้นที่ทำงาน **การเงินของร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="eb891-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="eb891-112">เมื่อต้องการเปลี่ยนมิติทางการเงินของธุรกรรม ให้เลือก **ออกแบบ** แล้วเลือกสัญลักษณ์ดินสอที่อยู่ถัดจากแถว **ธุรกรรม (ตรวจสอบได้)**</span><span class="sxs-lookup"><span data-stu-id="eb891-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="eb891-113">ค้นหาและเลือกฟิลด์ **FinancialDimensionDisplayValue** เลือกเซลล์ในส่วนหัวของเวิร์กชีต Excel แล้วเลือก **เพิ่มป้ายชื่อ**</span><span class="sxs-lookup"><span data-stu-id="eb891-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="eb891-114">เลือกเซลล์ใต้เซลล์ที่คุณเลือกในขั้นตอนก่อนหน้า ให้เลือก **เพิ่มค่า** แล้วเลือก **รีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="eb891-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="eb891-115">มิติทางการเงินจะถูกเพิ่มลงในเวิร์กชีต Excel จากนั้นจะสามารถแก้ไขและเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="eb891-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="eb891-116">เมื่อต้องการเปลี่ยนมิติในรายการธุรกรรม ให้เลือกแถว **ธุรกรรมการขาย (ตรวจสอบได้)** เลือกสัญลักษณ์ดินสอ แล้วทำซ้ำขั้นตอนที่ 6 และ 7</span><span class="sxs-lookup"><span data-stu-id="eb891-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="eb891-117">เมื่อต้องการเปลี่ยนมิติในรายการชำระเงิน ให้เลือกแถว **ธุรกรรมการชำระเงิน (ตรวจสอบได้)** เลือกสัญลักษณ์ดินสอ แล้วทำซ้ำขั้นตอนที่ 6 และ 7</span><span class="sxs-lookup"><span data-stu-id="eb891-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb891-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="eb891-118">Additional resources</span></span>

[<span data-ttu-id="eb891-119">แก้ไขและตรวจสอบธุรกรรมเงินสดและการขนส่งและการจัดการเงินสด</span><span class="sxs-lookup"><span data-stu-id="eb891-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="eb891-120">แก้ไขและตรวจสอบธุรกรรมใบสั่งออนไลน์และใบสั่งของลูกค้าแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="eb891-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="eb891-121">สร้างเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="eb891-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="eb891-122">เพิ่มฟิลด์ลงในเวิร์กบุ๊ก Excel เพื่อแก้ไขธุรกรรมการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="eb891-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]