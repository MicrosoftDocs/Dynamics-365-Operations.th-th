---
title: การคํานวณ TDS ในธุรกรรมระหว่างบริษัท
description: หัวข้อนี้อธิบายกระบวนการที่ใช้ในการคํานวณภาษีที่หักที่ต้นทาง (TDS) ในธุรกรรมระหว่างบริษัทในระยะต่างๆ
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
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023631"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="a2285-103">การคํานวณ TDS ในธุรกรรมระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="a2285-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2285-104">หัวข้อนี้อธิบายกระบวนการที่ใช้ในการคํานวณภาษีที่หักที่ต้นทาง (TDS) ในธุรกรรมระหว่างบริษัทในระยะต่างๆ</span><span class="sxs-lookup"><span data-stu-id="a2285-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="a2285-105">เมื่อมีการสร้างใบสั่งซื้อหรือใบสั่งขายระหว่างบริษัท กลุ่ม TDS เริ่มต้นที่กําหนดไว้สำหรับลูกค้าหรือผู้จัดจำหน่ายจะถูกใช้ในการคํานวณยอดเงิน TDS</span><span class="sxs-lookup"><span data-stu-id="a2285-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="a2285-106">มีการลงรายการบัญชียอดเงิน TDS ไปยังบัญชีลูกหนี้หรือบัญชีเจ้าหนี้ หลังจากที่มีการลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a2285-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="a2285-107">ใบสั่งขายหรือใบสั่งซื้อระหว่างบริษัทถูกสร้างขึ้นโดยอัตโนมัติสำหรับใบสั่งซื้อหรือใบสั่งขายต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="a2285-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="a2285-108">กลุ่ม TDS เริ่มต้นจะแสดงขึ้นบนใบสั่งระหว่างบริษัท เพื่อให้สามารถคํานวณ TDS ได้</span><span class="sxs-lookup"><span data-stu-id="a2285-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="a2285-109">คุณสามารถเปลี่ยนกลุ่ม TDS ได้</span><span class="sxs-lookup"><span data-stu-id="a2285-109">You can change the TDS group.</span></span> <span data-ttu-id="a2285-110">คุณสามารถลงรายการบัญชีใบแจ้งหนี้ได้เฉพาะเมื่อยอดเงินใบแจ้งหนี้สุทธิในใบสั่งระหว่างบริษัทที่สร้างขึ้นโดยอัตโนมัติตรงกับยอดเงินใบแจ้งหนี้สุทธิในใบสั่งต้นฉบับเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a2285-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="a2285-111">(ยอดเงินสุทธิคือจำนวนเงินของใบแจ้งหนี้ หลังจากหัก TDS แล้ว)</span><span class="sxs-lookup"><span data-stu-id="a2285-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="a2285-112">ตัวอย่างเช่น ใบแจ้งหนี้การขายจะถูกสร้างขึ้นสำหรับ 50,000 และมีการแนบกลุ่ม TDS **10%**</span><span class="sxs-lookup"><span data-stu-id="a2285-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="a2285-113">จำนวนเงินของใบแจ้งหนี้ที่ลงรายการบัญชีคือ 45,000 และยอดเงิน TDS ที่ลงรายการบัญชีสำหรับใบแจ้งหนี้การขายคือ 5,000</span><span class="sxs-lookup"><span data-stu-id="a2285-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="a2285-114">ระบบได้สร้างใบสั่งซื้อขึ้นโดยอัตโนมัติสำหรับใบสั่งขายระหว่างบริษัท และกลุ่ม TDS  **10%** จะถูกแนบอยู่</span><span class="sxs-lookup"><span data-stu-id="a2285-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="a2285-115">ถ้าคุณเปลี่ยนกลุ่ม TDS เป็น **15%** คุณจะลงรายการบัญชีใบแจ้งหนี้ไม่ได้ เนื่องจากจำนวนเงินของใบแจ้งหนี้สุทธิของใบสั่งขายระหว่างบริษัทที่สร้างขึ้นโดยอัตโนมัติไม่ตรงกับจำนวนเงินของใบแจ้งหนี้สุทธิของใบสั่งขายต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="a2285-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="a2285-116">มีการลงรายการบัญชีสมุดรายวันการชำระเงินที่ถูกสร้างขึ้นสำหรับใบแจ้งหนี้ระหว่างบริษัทโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a2285-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="a2285-117">สามารถลงรายการบัญชีสมุดรายวันการชำระเงินนั้นได้เฉพาะเมื่อยอดเงินที่ชำระสุทธิในนั้นตรงกับยอดเงินที่ชำระสุทธิในสมุดรายวันการชำระเงินต้นฉบับเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a2285-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
