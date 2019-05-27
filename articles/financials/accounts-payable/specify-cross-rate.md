---
title: ระบุอัตราไขว้
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับอัตราการข้ามใน Microsoft Dynamics 365 for Finance and Operations
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546075"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="83dd9-103">ระบุอัตราไขว้</span><span class="sxs-lookup"><span data-stu-id="83dd9-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83dd9-104">หัวข้อนี้อธิบายถึงวัตถุประสงค์ของอัตราไขว้ และวิธีการระบุอัตราไขว้เมื่อคุณชำระเงินด้วยใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="83dd9-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="83dd9-105">ใช้อัตราไขว้เมื่อเงื่อนไขต่อไปนี้ทั้งหมดใช้:</span><span class="sxs-lookup"><span data-stu-id="83dd9-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="83dd9-106">คุณกำลังชำระบัญชีการชำระเงิน ด้วยใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="83dd9-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="83dd9-107">บรรทัดการชำระเงินและบรรทัดใบแจ้งหนี้ใช้สกุลเงินอื่น</span><span class="sxs-lookup"><span data-stu-id="83dd9-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="83dd9-108">ไม่มีสกุลเงินที่เป็นสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="83dd9-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="83dd9-109">ไม่มีการใช้อัตราไขว้เพื่อคำนวณการแปลงสกุลเงินของธุรกรรมการชำระเงินเป็นการชำระเงินสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="83dd9-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="83dd9-110">อัตราแลกเปลี่ยนจากตารางอัตราแลกเปลี่ยน จะถูกดึงมาคำนวณมูลค่าของยอดเงินสกุลเงินของธุรกรรมการชำระเงินและยอดสกุลเงินทางบัญชีการชำระเงินแทน</span><span class="sxs-lookup"><span data-stu-id="83dd9-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="83dd9-111">ตัวอย่างเช่น สกุลเงินทางบัญชีคือ USD สกุลเงินใบแจ้งหนี้คือ CAD และสกุลเงินการชำระเงินคือ EUR </span><span class="sxs-lookup"><span data-stu-id="83dd9-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="83dd9-112">อัตราไขว้ช่วยให้คุณสามารถป้อนอัตราแลกเปลี่ยนเพื่อแปลโดยตรงระหว่าง CAD และ EUR และไม่ต้องแปลผ่าน USD</span><span class="sxs-lookup"><span data-stu-id="83dd9-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="83dd9-113">เมื่อคุณเลือกใบแจ้งหนี้และการชำระเงินหลัก คุณสามารถป้อนอัตราแลกเปลี่ยนคร่อมสำหรับบรรทัดใบแจ้งหนี้ได้ </span><span class="sxs-lookup"><span data-stu-id="83dd9-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="83dd9-114">อัตราไขว้คือ อัตราแลกเปลี่ยนระหว่างสกุลเงินสำหรับธุรกรรม ณ วันชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="83dd9-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="83dd9-115">ไปยังหน้าใดหน้าหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="83dd9-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="83dd9-116">**บัญชีลูกหนี้ > ทั่วไป > ลูกค้า > ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="83dd9-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="83dd9-117">**บัญชีเจ้าหนี้ > ทั่วไป > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="83dd9-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="83dd9-118">**การจัดซื้อและการจัดหา > ทั่วไป > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="83dd9-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="83dd9-119">เลือกลูกค้าหรือผู้จำหน่ายที่มีธุรกรรมที่เปิดค้างไว้ซึ่งคุณกำลังชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="83dd9-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="83dd9-120">สำหรับลูกค้า บนหน้ารายการ **ลูกค้าทั้งหมด** ไปยัง **รวบรวม > ชำระธุรกรรมที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="83dd9-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="83dd9-121">สำหรับผู้จัดจำหน่าย บนหน้ารายการ **ผู้จัดจำหน่ายทั้งหมด** ไปยัง **ใบแจ้งหนี้ > ชำระธุรกรรมที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="83dd9-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="83dd9-122">เลือกธุรกรรมที่เป็นการชำระเงินหลัก แล้วจากนั้น คลิก **ทำเครื่องหมายการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="83dd9-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="83dd9-123">กล่องกาเครื่องหมายในคอลัมน์ **ทำเครื่องหมาย** จะถูกเลือก และไอคอนข้อมูลจะแสดงในคอลัมน์ **การชำระเงินหลัก**</span><span class="sxs-lookup"><span data-stu-id="83dd9-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="83dd9-124">ในฟิลด์ **อัตราไขว้** ให้ป้อนอัตราแลกเปลี่ยนระหว่างสกุลเงินใบแจ้งหนี้และสกุลเงินการชำระเงิน ณ วันที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="83dd9-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
