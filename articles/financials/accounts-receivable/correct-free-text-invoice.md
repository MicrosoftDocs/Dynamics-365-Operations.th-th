---
title: แก้ไขใบแจ้งหนี้ข้อความอิสระ
description: บทความนี้อธิบายวิธีการแก้ไขข้อความอิสระในใบแจ้งหนี้ที่ได้ลงรายการบัญชี และออกใบแจ้งหนี้ที่แก้ไขใหม่
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c1b90b7b2c02a53e53cc13d70445a237b126d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559790"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="1d3e8-103">แก้ไขใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="1d3e8-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d3e8-104">บทความนี้อธิบายวิธีการแก้ไขข้อความอิสระในใบแจ้งหนี้ที่ได้ลงรายการบัญชี และออกใบแจ้งหนี้ที่แก้ไขใหม่</span><span class="sxs-lookup"><span data-stu-id="1d3e8-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="1d3e8-105">เมื่อต้องการแก้ไขใบแจ้งหนี้ข้อความอิสระที่ลงรายการบัญชีเรียบร้อยแล้ว เปิดใบแจ้งหนี้ข้อความอิสระที่ลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="1d3e8-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="1d3e8-106">ในหน้า **ใบแจ้งหนี้** เลือก**ยกเลิก**แล้วเลือก **แก้ไขใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="1d3e8-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="1d3e8-107">เลือกรหัสเหตุผล เพิ่มข้อคิดเห็น และเลือกวันที่สำหรับใบแจ้งหนี้ใหม่ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="1d3e8-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="1d3e8-108">คุณสามารถปรับเปลี่ยนใบแจ้งหนี้ที่แก้ไขแล้ว และลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="1d3e8-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="1d3e8-109">เมื่อคุณลงรายการบัญชีใบแจ้งหนี้ที่แก้ไขแล้ว มีการสร้างใบแจ้งหนี้ที่ยกเลิกสำหรับยอดเงินเครดิตซึ่งเท่ากับยอดใบแจ้งหนี้ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="1d3e8-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="1d3e8-110">ดังนั้น ยอดดุลรวมของใบแจ้งหนี้ต้นฉบับและใบแจ้งหนี้ที่ยกเลิกเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="1d3e8-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="1d3e8-111">ใบแจ้งหนี้ที่ยกเลิกถูกจับคู่กับใบแจ้งหนี้ต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="1d3e8-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="1d3e8-112">หลังจากที่คุณลงรายการบัญชีใบแจ้งหนี้ที่แก้ไขแล้ว คุณจะมีสามใบแจ้งหนี้:</span><span class="sxs-lookup"><span data-stu-id="1d3e8-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="1d3e8-113">**ใบแจ้งหนี้ต้นฉบับ** – ใบแจ้งหนี้ที่ประกอบด้วยข้อมูลที่คุณกำลังแก้ไข</span><span class="sxs-lookup"><span data-stu-id="1d3e8-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="1d3e8-114">**ใบแจ้งหนี้ที่ยกเลิก**– ใบแจ้งหนี้เงินเชื่อที่ระบบสร้างขึ้นที่ถูกสร้างขึ้นเพื่อยกเลิกใบแจ้งหนี้ที่มีแก้ไขล่าสุด</span><span class="sxs-lookup"><span data-stu-id="1d3e8-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="1d3e8-115">**ใบแจ้งหนี้ที่แก้ไขแล้ว** – ใบแจ้งหนี้ที่ประกอบด้วยข้อมูลใบแจ้งหนี้ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="1d3e8-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="1d3e8-116">คุณสามารถระบุการยกเลิกและการแก้ไขใบแจ้งหนี้ในสองวิธี:</span><span class="sxs-lookup"><span data-stu-id="1d3e8-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="1d3e8-117">หน้า **ใบแจ้งหนี้ข้อความอิสระทั้งหมด** ประกอบด้วยการคอลัมน์ **การแก้ไข** ซึ่งคุณสามารถดูใบแจ้งหนี้ที่เป็นใบแจ้งหนี้ที่ยกเลิกและใบแจ้งหนี้ที่แก้ไขแล้ว</span><span class="sxs-lookup"><span data-stu-id="1d3e8-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="1d3e8-118">ส่วนหัวของใบแจ้งหนี้ข้อความอิสระแสดงสถานะของ **ใบแจ้งหนี้ที่ยกเลิก '\[หมายเลขใบแจ้งหนี้\]'** หรือ **ใบแจ้งหนี้ที่แก้ไขแล้ว '\[หมายเลขใบแจ้งหนี้\]'**</span><span class="sxs-lookup"><span data-stu-id="1d3e8-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="1d3e8-119">คุณสมบัตินี้จะสามารถใช้งานได้ก็ต่อเมื่อคีย์การตั้งค่าคอนฟิก **การแก้ไขใบแจ้งหนี้ข้อความอิสระ** มีการเลือก</span><span class="sxs-lookup"><span data-stu-id="1d3e8-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>



