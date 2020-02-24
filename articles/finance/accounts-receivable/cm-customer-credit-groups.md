---
title: กลุ่มสินเชื่อลูกค้า
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับกลุ่มเครดิตของลูกค้า
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015416"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="49911-103">กลุ่มสินเชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49911-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="49911-104">คุณสามารถกำหนดกลุ่มของลูกค้าที่มีวงเงินสินเชื่อเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="49911-104">You can define groups of customers who have the same credit limit.</span></span> <span data-ttu-id="49911-105">นอกจากนี้ ยังมีการพิจารณาวงเงินสินเชื่อแต่ละรายการที่ถูกกำหนดไว้ในบัญชีใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49911-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="49911-106">สามารถเลือกสมาชิกของกลุ่มเครดิตลูกค้าได้จากนิติบุคคลที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="49911-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="49911-107">เมื่อคุณเพิ่มลูกค้าลงในรายชื่อลูกค้าในกลุ่มเครดิตของลูกค้า จะมีการเปลี่ยนแปลงวันหมดอายุของวงเงินสินเชื่อสำหรับลูกค้าแต่ละรายเป็นวันหมดอายุที่ถูกกำหนดให้กับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="49911-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="49911-108">คุณสามารถตั้งค่ากลุ่มเครดิตของลูกค้าใน **กลุ่มเครดิตของลูกค้า** (**การจัดการสินเชื่อ \> กลุ่มเครดิตของลูกค้า \> กลุ่มเครดิตของลูกค้า**)</span><span class="sxs-lookup"><span data-stu-id="49911-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="49911-109">ในฟิลด์ **หมายเลขกลุ่ม** และ **คำอธิบาย** ให้ป้อนตัวระบุและคำอธิบายสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="49911-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="49911-110">ในฟิลด์ **วงเงินสินเชื่อ** และ **สกุลเงิน** ให้ป้อนวงเงินสินเชื่อและสกุลเงินที่ควรใช้เมื่อระบบตรวจสอบวงเงินสินเชื่อสำหรับสมาชิกใดๆ ของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="49911-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="49911-111">ในฟิลด์ **วันที่สิ้นสุดวงเงินสินเชื่อ** ให้ป้อนวันที่ที่วงเงินสินเชื่อหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="49911-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="49911-112">กลุ่มเครดิตของลูกค้าต้องมีวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="49911-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="49911-113">หลังจากที่คุณตั้งค่ากลุ่มเครดิตของลูกค้าเสร็จแล้ว คุณสามารถเพิ่มลูกค้าลงในกลุ่มได้โดยการระบุนิติบุคคลและรหัสบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49911-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="49911-114">เมื่อคุณเพิ่มลูกค้าใหม่เข้าในกลุ่มเครดิตของลูกค้า ระบบจะค้นหาบัญชีลูกค้าเดียวกันระหว่างนิติบุคคลทั้งหมด และแจ้งให้คุณเพิ่มลูกค้าในกลุ่มเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49911-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="49911-115">ใช้เมนู **ยอดดุลตามอายุหนี้** เพื่อดูรายละเอียดของยอดดุลอายุหนี้สำหรับลูกค้าในใบแจ้งหนี้ทั้งหมดในกลุ่มเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="49911-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="49911-116">หน้า **ยอดดุลอายุหนี้** จะแสดงสรุปของยอดดุลตามอายุหนี้สำหรับบัญชีลูกค้าในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="49911-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
