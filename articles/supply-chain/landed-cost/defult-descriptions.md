---
title: คำอธิบายเริ่มต้นเกี่ยวกับบัญชีแยกประเภททั่วไป
description: คุณสามารถใช้คำอธิบายเริ่มต้นเพื่ออัพเดตฟิลด์ คำอธิบาย ในการลงรายการบัญชีใบสำคัญในบัญชีแยกประเภททั่วไป
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500391"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="a237b-103">คำอธิบายเริ่มต้นเกี่ยวกับบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a237b-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a237b-104">คุณสามารถใช้คำอธิบายเริ่มต้นเพื่ออัพเดตฟิลด์ **คำอธิบาย** ในการลงรายการบัญชีใบสำคัญในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="a237b-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="a237b-105">ฟังก์ชันนี้ได้รับการปรับปรุงให้ใช้งานกับต้นทุนแฝง</span><span class="sxs-lookup"><span data-stu-id="a237b-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="a237b-106">เมื่อต้องการตั้งค่าคำอธิบายเริ่มต้นสำหรับการลงรายการบัญชีแยกประเภท ให้ไปที่ **การจัดการองค์กร \> การตั้งค่า \> คำอธิบายเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="a237b-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="a237b-107">ตารางต่อไปนี้จะแสดงรายการค่าใหม่ที่มีการเพิ่มไว้สำหรับฟิลด์ **คำอธิบาย** ในหน้า **คำอธิบายเริ่มต้น** เพื่อสนับสนุนต้นทุนแฝง</span><span class="sxs-lookup"><span data-stu-id="a237b-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="a237b-108">ชนิดคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a237b-108">Description type</span></span> | <span data-ttu-id="a237b-109">บันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="a237b-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="a237b-110">การคิดต้นทุนการนําเข้า – การค้างรับค้างจ่ายต้นทุน</span><span class="sxs-lookup"><span data-stu-id="a237b-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="a237b-111">เมื่อมีการลงรายการบัญชีใบแจ้งหนี้ใบสั่งซื้อ การค้างรับค้างจ่ายต้นทุนจะถูกประมวลผลสำหรับต้นทุนการเดินทางโดยประมาณ</span><span class="sxs-lookup"><span data-stu-id="a237b-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="a237b-112">สามารถระบุรายละเอียดเริ่มต้นเพื่อเพิ่มหมายเลขการเดินทางไปยังคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a237b-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="a237b-113">ใช้ *%4* สำหรับหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="a237b-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="a237b-114">การคิดต้นทุนการนำเข้า – ใบสั่งสินค้าที่อยู่ระหว่างส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="a237b-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="a237b-115">ถ้าคุณใช้การประมวลผลระหว่างการส่งต่อ มีการลงรายการบัญชีใบแจ้งหนี้ใบสั่งซื้อ และมีการลงรายการบัญชีสินค้าในบัญชีสินค้าที่อยู่ระหว่างส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="a237b-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="a237b-116">สามารถระบุคำอธิบายเริ่มต้นเพื่อเพิ่มหมายเลขใบสั่งระหว่างส่งต่อไปยังคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a237b-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="a237b-117">ใช้ *%4* สำหรับหมายเลขใบสั่งระหว่างส่งต่อ</span><span class="sxs-lookup"><span data-stu-id="a237b-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="a237b-118">สินค้าคงคลัง – ปิด – การปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="a237b-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="a237b-119">เมื่อใบแจ้งหนี้ของบัญชีเจ้าหนี้ (AP) มีการประมวลผลสำหรับต้นทุนการเดินทาง การปรับปรุงสินค้าคงคลังจะถูกประมวลผลเพื่อประเมินต้นทุนการเดินทาง</span><span class="sxs-lookup"><span data-stu-id="a237b-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="a237b-120">สามารถระบุรายละเอียดเริ่มต้นเพื่อเพิ่มหมายเลขการเดินทางไปยังคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a237b-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="a237b-121">ใช้ *%4* สำหรับหมายเลขการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="a237b-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="a237b-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานกับหน้า **คำอธิบายเริ่มต้น** โปรดดูที่ [ตั้งค่าคำอธิบายเริ่มต้นสำหรับการลงรายการบัญชีอัตโนมัติ](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md)</span><span class="sxs-lookup"><span data-stu-id="a237b-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
