---
title: สมุดรายวันสมดุลสำหรับการบัญชีระหว่างหน่วย
description: บทความนี้แสดงวิธีที่สมุดรายวันกำหนดยอดดุลโดยอัตโนมัติ เมื่อเลือกมิติทางการเงินยอดดุลในหน้าบัญชีแยกประเภท
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839364"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="95cd5-103">สมุดรายวันสมดุลสำหรับการบัญชีระหว่างหน่วย</span><span class="sxs-lookup"><span data-stu-id="95cd5-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95cd5-104">บทความนี้แสดงวิธีที่สมุดรายวันกำหนดยอดดุลโดยอัตโนมัติ เมื่อเลือกมิติทางการเงินยอดดุลในหน้าบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="95cd5-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="95cd5-105">ถ้ารายการบัญชีไม่สมดุลในระดับของค่ามิติทางการเงิน รายการบัญชีเพิ่มเติมจะถูกสร้างขึ้นโดยอัตโนมัติในดุลสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="95cd5-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="95cd5-106">รายการบัญชีเหล่านี้ใช้ **ระหว่างหน่วย - เดบิต** และ**ระหว่างหน่วย - เครดิต** การลงชนิดรายการบัญชีในหน้า **สำหรับหน้าธุรกรรมอัตโนมัติ** เพื่อกำหนดบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="95cd5-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="95cd5-107">ตัวอย่างเช่น หน่วยธุรกิจ ซึ่งเป็นส่วนที่สองของบัญชีแยกประเภท ถูกเลือกเป็นมิติทางการเงินของยอดดุล และกำลังจะมีสร้างรายการบัญชีต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="95cd5-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="95cd5-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="95cd5-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="95cd5-109">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="95cd5-109">100.00 DR</span></span> |
| <span data-ttu-id="95cd5-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="95cd5-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="95cd5-111">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="95cd5-111">100.00 DR</span></span> |
| <span data-ttu-id="95cd5-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="95cd5-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="95cd5-113">200.00 CR</span><span class="sxs-lookup"><span data-stu-id="95cd5-113">200.00 CR</span></span> |

<span data-ttu-id="95cd5-114">ในกรณีนี้ มีกำหนดยอดดุลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="95cd5-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="95cd5-115">สำหรับหน่วยธุรกิจ MSP = 100.00 CR</span><span class="sxs-lookup"><span data-stu-id="95cd5-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="95cd5-116">สำหรับหน่วยธุรกิจ NY = 100.00 DR</span><span class="sxs-lookup"><span data-stu-id="95cd5-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="95cd5-117">ดังนั้น รายการบัญชีต่อไปนี้จะสร้างขึ้นโดยอัตโนมัติ เพื่อให้รายการสมุดรายวันนี้สมดุลที่ระดับค่ามิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="95cd5-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="95cd5-118">(ระหว่างหน่วยเดบิต) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="95cd5-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="95cd5-119">100.00 DR</span><span class="sxs-lookup"><span data-stu-id="95cd5-119">100.00 DR</span></span> |
| <span data-ttu-id="95cd5-120">(ระหว่างหน่วยเครดิต) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="95cd5-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="95cd5-121">100.00 CR</span><span class="sxs-lookup"><span data-stu-id="95cd5-121">100.00 CR</span></span> |





