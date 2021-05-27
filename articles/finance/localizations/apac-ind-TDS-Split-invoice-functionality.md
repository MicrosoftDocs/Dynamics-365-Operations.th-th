---
title: ฟังก์ชันแบ่งใบแจ้งหนี้
description: หัวข้อนี้อธิบายการตั้งค่าและฟังก์ชันในการแบ่งใบแจ้งหนี้ตามที่อยู่ที่จัดส่งและหมายเลขบัญชีภาษี (TAN)
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023633"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="cffb3-103">ฟังก์ชันแบ่งใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="cffb3-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cffb3-104">หัวข้อนี้อธิบายการตั้งค่าและฟังก์ชันในการแบ่งใบแจ้งหนี้ตามที่อยู่ที่จัดส่งและหมายเลขบัญชีภาษี (TAN)</span><span class="sxs-lookup"><span data-stu-id="cffb3-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="cffb3-105">บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** บนแท็บ **ทั่วไป** ให้เลือกกล่องกาเครื่องหมาย **ใบรับสินค้า** หรือ **ใบแจ้งหนี้** เพื่อลงรายการบัญชี และแบ่งใบรับสินค้าหรือใบแจ้งหนี้ที่มีที่อยู่ที่จัดส่งและ TAN ที่แตกต่างกันบนหน้า **ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="cffb3-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="cffb3-106">จากนั้น ใบแจ้งหนี้ที่ลงรายการบัญชีแล้วจะถูกแบ่งตามที่อยู่ที่จัดส่งและ TAN</span><span class="sxs-lookup"><span data-stu-id="cffb3-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="cffb3-107">บนแท็บ **การอัพเดตสรุป** บน FastTab **แบ่งตาม** ในแถว **ข้อมูลการจัดส่ง** ให้ตั้งค่าตัวเลือก **การยืนยัน**, **รายการเบิกสินค้า**, **บันทึกการจัดส่ง** หรือ **ใบแจ้งหนี้** เป็น **ใช่** เพื่อลงรายการบัญชีและแบ่งการยืนยัน รายการเบิกสินค้า บันทึกการจัดส่ง หรือใบแจ้งหนี้ ซึ่งมีการกําหนดที่อยู่ที่จัดส่งและ TAN ที่แตกต่างกันให้กับบรรทัดใบแจ้งหนี้ต่างๆ บนหน้า **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="cffb3-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="cffb3-108">อันดับแรกใบแจ้งหนี้จะถูกแบ่งตามที่อยู่ที่จัดส่ง และจากนั้นตาม TAN</span><span class="sxs-lookup"><span data-stu-id="cffb3-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="cffb3-109">ถ้าไม่มีตัวเลือกใดๆ สำหรับ **ข้อมูลการจัดส่ง** ถูกตั้งค่าเป็น **ใช่** จะมีการลงรายการบัญชีใบแจ้งหนี้เป็นใบแจ้งหนี้เดียว</span><span class="sxs-lookup"><span data-stu-id="cffb3-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="cffb3-110">จะไม่มีการแบ่งใบแจ้งหนี้เกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="cffb3-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="cffb3-111">เมื่อต้องการแบ่งและลงรายการบัญชีบันทึกการจัดส่งซึ่งรายการใบแจ้งหนี้มีที่อยู่ที่จัดส่งและ TAN ที่แตกต่างกัน คุณต้องตั้งค่าตัวเลือก **บันทึกการจัดส่ง** สำหรับ **ข้อมูลการจัดส่ง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cffb3-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="cffb3-112">เมื่อต้องการแบ่งและลงรายการบัญชีใบแจ้งหนี้ซึ่งรายการใบแจ้งหนี้มีที่อยู่ที่จัดส่งและ TAN ที่แตกต่างกัน คุณต้องตั้งค่าตัวเลือก **ใบแจ้งหนี้** สำหรับ **ข้อมูลการจัดส่ง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="cffb3-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="cffb3-113">เมื่อต้องการลงรายการบัญชีใบแจ้งหนี้ซึ่งรายการใบแจ้งหนี้มีที่อยู่ที่จัดส่งที่แตกต่างกัน แต่ TAN เดียวกัน ให้ตั้งค่าตัวเลือก **ใบแจ้งหนี้** สำหรับ **ข้อมูลการจัดส่ง** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="cffb3-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="cffb3-114">ใบแจ้งหนี้จะถูกแบ่งตามที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="cffb3-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="cffb3-115">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="cffb3-115">Example</span></span>

<span data-ttu-id="cffb3-116">ในตัวอย่างนี้ ตัวเลือก **ใบแจ้งหนี้** สำหรับ **ข้อมูลการจัดส่ง** จะถูกตั้งค่าเป็น **ใช่** บนแท็บ **การอัพเดตสรุป** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="cffb3-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="cffb3-117">มีการลงรายการบัญชีใบแจ้งหนี้การซื้อซึ่งมีการตั้งค่าต่อไปนี้สำหรับที่อยู่ที่จัดส่งและ TAN ในรายการต่างๆ:</span><span class="sxs-lookup"><span data-stu-id="cffb3-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="cffb3-118">**รายการสินค้า 1:** ที่อยู่ที่จัดส่ง 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="cffb3-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="cffb3-119">**รายการสินค้า 2:** ที่อยู่ที่จัดส่ง 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="cffb3-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="cffb3-120">**รายการสินค้า 3:** ที่อยู่ที่จัดส่ง 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="cffb3-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="cffb3-121">**รายการสินค้า 4:** ที่อยู่ที่จัดส่ง 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="cffb3-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="cffb3-122">ในกรณีนี้ ใบแจ้งหนี้ต้นฉบับจะถูกแบ่งออกเป็นใบแจ้งหนี้สองใบ และถูกลงรายการบัญชีในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cffb3-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="cffb3-123">มีการลงรายการบัญชีใบแจ้งหนี้ 1 สำหรับรายการสินค้า 1 และรายการสินค้า 2 เนื่องจากทั้งสองรายการมีที่อยู่ที่จัดส่งและ TAN เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="cffb3-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="cffb3-124">ใบแจ้งหนี้ 2 ถูกลงรายการบัญชีสำหรับรายการสินค้า 3</span><span class="sxs-lookup"><span data-stu-id="cffb3-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="cffb3-125">ใบแจ้งหนี้ 3 ถูกลงรายการบัญชีสำหรับรายการสินค้า 4</span><span class="sxs-lookup"><span data-stu-id="cffb3-125">Invoice 3 is posted for item line 4.</span></span>
