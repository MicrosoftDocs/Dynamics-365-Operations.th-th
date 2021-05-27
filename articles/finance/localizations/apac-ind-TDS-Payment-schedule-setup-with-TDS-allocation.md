---
title: ตั้งค่ากำหนดการชำระเงินด้วยการปันส่วน TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่ากำหนดการชำระเงินด้วยการปันส่วนภาษี ณ ที่จ่าย (TDS)
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023636"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="f5ef1-103">ตั้งค่ากำหนดการชำระเงินด้วยการปันส่วน TDS</span><span class="sxs-lookup"><span data-stu-id="f5ef1-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5ef1-104">หัวข้อนี้อธิบายวิธีการตั้งค่ากำหนดการชำระเงินด้วยการปันส่วนภาษี ณ ที่จ่าย (TDS)</span><span class="sxs-lookup"><span data-stu-id="f5ef1-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="f5ef1-105">ไปที่ **บัญชีเจ้าหนี้ \> การตั้งค่าการชำระเงิน \> กำหนดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="f5ef1-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="f5ef1-106">[![หน้ากำหนดการชำระเงิน](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="f5ef1-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="f5ef1-107">ในบานหน้าต่างการดำเนินการ เลือก **ใหม่** เพื่อสร้างกำหนดการชำระเงิน และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f5ef1-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="f5ef1-108">ในฟิลด์ **การปันส่วน** เลือกวิธีที่จะปันส่วนการชำระเงินสำหรับกำหนดการชำระเงิน:</span><span class="sxs-lookup"><span data-stu-id="f5ef1-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="f5ef1-109">ผลรวม</span><span class="sxs-lookup"><span data-stu-id="f5ef1-109">Total</span></span>
    - <span data-ttu-id="f5ef1-110">ยอดเงินคงที่</span><span class="sxs-lookup"><span data-stu-id="f5ef1-110">Fixed amount</span></span>
    - <span data-ttu-id="f5ef1-111">ปริมาณคงที่</span><span class="sxs-lookup"><span data-stu-id="f5ef1-111">Fixed quantity</span></span>
    - <span data-ttu-id="f5ef1-112">ที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f5ef1-112">Specified</span></span>

    <span data-ttu-id="f5ef1-113">ฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** แสดงวิธีการปันส่วน TDS สำหรับกำหนดการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f5ef1-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="f5ef1-114">ถ้าคุณเลือก **ผลรวม** ในฟิลด์ **การปันส่วน** ฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** จะถูกตั้งค่าเป็น **ผลรวม** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f5ef1-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="f5ef1-115">ถ้าคุณเลือก **ยอดเงินคงที่** **ปริมาณคงที่** หรือ **ที่ระบุ** ในฟิลด์ **การปันส่วน** ฟิลด์ **การปันส่วน ภาษีหัก ณ ที่จ่าย** จะถูกตั้งค่าเป็น **ตามสัดส่วน** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f5ef1-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5ef1-116">หากฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** มีการตั้งค่าเป็น **ยอดรวม** งวดการชำระเงินจะคำนวณตามยอดเงินรวม ซึ่งรวมถึงยอดเงิน TDS ด้วย</span><span class="sxs-lookup"><span data-stu-id="f5ef1-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="f5ef1-117">หากฟิลด์ **การปันส่วนภาษีหัก ณ ที่จ่าย** มีการตั้งค่าเป็น **ตามสัดส่วน** งวดการชำระเงินจะคำนวณตามยอดเงินสุทธิตามใบแจ้งหนี้ หลังหักยอดเงิน TDS</span><span class="sxs-lookup"><span data-stu-id="f5ef1-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="f5ef1-118">ป้อนรายละเอียดอื่นๆ ที่จำเป็น แล้วปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f5ef1-118">Enter the other required details, and then close the page.</span></span>
