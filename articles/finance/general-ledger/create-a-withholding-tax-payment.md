---
title: สร้างการชำระภาษี ณ ที่จ่าย
description: ขั้นตอนการชำระภาษีหัก ณ ที่จ่ายจะกำหนดยอดภาษีหัก ณ ที่จ่ายจากบัญชีที่ต้องชำระในบัญชีภาษีหัก ณ ที่จ่ายและหักลบเป็นบัญชีหักภาษี ณ ที่จ่ายสำหรับช่วงเวลาที่กำหนด หัวข้อนี้แสดงรายการขั้นตอนของการตั้งค่าการชำระภาษีหัก ณ ที่จ่าย
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 72d80fbb3b2448f4b89fa7d7fa580387e1a3621c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832957"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="0ea92-104">สร้างการชำระภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="0ea92-104">Create a withholding tax payment</span></span>

<span data-ttu-id="0ea92-105">ขั้นตอนการชำระภาษีหัก ณ ที่จ่ายจะกำหนดยอดภาษีหัก ณ ที่จ่ายจากบัญชีที่ต้องชำระในบัญชีภาษีหัก ณ ที่จ่ายและหักลบเป็นบัญชีหักภาษี ณ ที่จ่ายสำหรับช่วงเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="0ea92-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="0ea92-106">หัวข้อนี้แสดงรายการขั้นตอนของการตั้งค่าการชำระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="0ea92-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="0ea92-107">การชดเชยภาษีหัก ณ ที่จ่าย (จากบัญชีลูกหนี้) จะไม่ถูกพิจารณาเมื่อมีการคํานวณการหักภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="0ea92-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="0ea92-108">ไปที่ **บานหน้าต่างการนำทาง > โมดูล > ภาษี > การประกาศ > ภาษีหัก ณ ที่จ่าย > การชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="0ea92-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="0ea92-109">ในฟิลด์ **รอบระยะเวลาการจ่ายเงิน** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="0ea92-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0ea92-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0ea92-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0ea92-111">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0ea92-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="0ea92-112">ในฟิลด์ **วันที่ทำธุรกรรม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="0ea92-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="0ea92-113">เลือก **อัปเดต** เพื่อลงรายการบัญชีใบสำคัญจ่ายภาษีหัก ณ ที่จ่ายไปยังบัญชีหักภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="0ea92-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="0ea92-114">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0ea92-114">Click **OK**.</span></span>

![พารามิเตอร์การชำระภาษีหัก ณ ที่จ่าย](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]