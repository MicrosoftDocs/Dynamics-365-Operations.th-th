---
title: "ยอดดุลบัญชีแยกประเภททั่วไป"
description: "บทความนี้อธิบายถึงสองวิธีในการดูยอดดุลบัญชีแยกประเภททั่วไป - หน้ารายการงบทดลองและรายงานทางการเงิน นอกจากนี้ยังอธิบายวิธีการปรับปรุงยอดดุลของเซ็ตมิติ"
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13191
ms.assetid: ea3650ac-34a0-4516-b75b-801c2164107d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 47336a19899b1fad0e63265173fd7fd02fc74ec3
ms.openlocfilehash: 0f87e82655ac9fa83ee116d0698b38804cfbf55c
ms.contentlocale: th-th
ms.lasthandoff: 01/12/2018

---

# <a name="general-ledger-account-balances"></a><span data-ttu-id="9e900-104">ยอดดุลบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9e900-104">General ledger account balances</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9e900-105">บทความนี้อธิบายถึงสองวิธีในการดูยอดดุลบัญชีแยกประเภททั่วไป - หน้ารายการงบทดลองและรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9e900-105">This article explains two ways to view general ledger account balances -  the Trial balance list page and financial reports.</span></span> <span data-ttu-id="9e900-106">นอกจากนี้ยังอธิบายวิธีการปรับปรุงยอดดุลของเซ็ตมิติ</span><span class="sxs-lookup"><span data-stu-id="9e900-106">It also discusses how to update dimension set balances.</span></span>

<span data-ttu-id="9e900-107">มีหลายวิธีที่ผู้ใช้สามารถดูยอดดุล ในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="9e900-107">There are a variety of ways users can view balances in the general ledger.</span></span> <span data-ttu-id="9e900-108">ตัวเลือกทั่วไปบางตัวเลือกที่พบมากที่สุดได้แก่:</span><span class="sxs-lookup"><span data-stu-id="9e900-108">Some of the most common options are:</span></span>

-   <span data-ttu-id="9e900-109">งบทดลอง</span><span class="sxs-lookup"><span data-stu-id="9e900-109">Trial balance</span></span>
-   <span data-ttu-id="9e900-110">รายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9e900-110">Financial reports</span></span>
-   <span data-ttu-id="9e900-111">ธุรกรรมใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="9e900-111">Voucher transactions</span></span>
-   <span data-ttu-id="9e900-112">รายงานบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9e900-112">Ledger reports</span></span>

<span data-ttu-id="9e900-113">วิธีธรรมดาที่สุดคือ หน้ารายการงบทดลองและรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9e900-113">The most common ways are the trial balance list page and financial reports.</span></span>

## <a name="trial-balance"></a><span data-ttu-id="9e900-114">งบทดลอง</span><span class="sxs-lookup"><span data-stu-id="9e900-114">Trial balance</span></span>
<span data-ttu-id="9e900-115">งบทดลองคือ หน้ารายการที่แสดงยอดดุลของบัญชีผู้ใช้และ/หรือมิติทั้งหมดสำหรับรอบระยะเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="9e900-115">The trial balance is a list page that shows all of the balances of an account and/or dimensions for a given period of time.</span></span> <span data-ttu-id="9e900-116">เมื่อเปิดงบทดลองก่อน งบทดลองจะรีเฟรชด้วยยอดดุลสำหรับวันและคุณสมบัติที่ตั้งค่าในพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="9e900-116">When the trial balance is first opened it refreshes with the balances for the dates and properties that are set in the Parameters.</span></span> <span data-ttu-id="9e900-117">คุณสมบัติที่สามารถเปลี่ยนแปลงในพารามิเตอร์คือ วันที่ ชั้นที่ลงรายการบัญชี วิธีที่พวกเขาต้องการเปิดยอดดุลให้แสดงอยู่ และชนิดของธุรกรรมปิดบัญชีจะแสดงการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="9e900-117">Properties that can be changed in Parameters are the dates, posting layer, how they want opening balances to appear, and what closing transaction types to show.</span></span> 

<span data-ttu-id="9e900-118">เมื่อผู้ใช้เปลี่ยนพารามิเตอร์ ยอดดุลจะรีเฟรช</span><span class="sxs-lookup"><span data-stu-id="9e900-118">When a user changes the parameters the balances are refreshed.</span></span> <span data-ttu-id="9e900-119">ผู้ใช้ยังสามารถเลือกเซ็ตมิติ พวกเขาต้องการดูยอดดุล ว่าแต่ละมิติจะแสดงในคอลัมน์ที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="9e900-119">The user can also pick what dimension set they want to view balances for and whether each of the dimensions show in separate columns.</span></span> 

<span data-ttu-id="9e900-120">ผู้ใช้สามารถสามารถดูรายละเอียดแนวลึกของยอดดุลต่างๆ เพื่อดูธุรกรรมที่สร้างยอดดุลนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="9e900-120">Users can drill down on the balances to view the transactions that make up the balance.</span></span>    

<span data-ttu-id="9e900-121">สำหรับข้อมูลเพิ่มเติม ดู [ดูรายงานทางการเงิน](view-financial-reports.md)</span><span class="sxs-lookup"><span data-stu-id="9e900-121">For more information, see [View financial reports](view-financial-reports.md).</span></span>




