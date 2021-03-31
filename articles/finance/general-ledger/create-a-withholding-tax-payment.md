---
title: สร้างการชำระภาษี ณ ที่จ่าย
description: ขั้นตอนการชำระภาษีหัก ณ ที่จ่ายจะกำหนดยอดภาษีหัก ณ ที่จ่ายจากบัญชีที่ต้องชำระในบัญชีภาษีหัก ณ ที่จ่ายและหักลบเป็นบัญชีหักภาษี ณ ที่จ่ายสำหรับช่วงเวลาที่กำหนด หัวข้อนี้แสดงรายการขั้นตอนของการตั้งค่าการชำระภาษีหัก ณ ที่จ่าย
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212288"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="d593c-104">สร้างการชำระภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="d593c-104">Create a withholding tax payment</span></span>

<span data-ttu-id="d593c-105">ขั้นตอนการชำระภาษีหัก ณ ที่จ่ายจะกำหนดยอดภาษีหัก ณ ที่จ่ายจากบัญชีที่ต้องชำระในบัญชีภาษีหัก ณ ที่จ่ายและหักลบเป็นบัญชีหักภาษี ณ ที่จ่ายสำหรับช่วงเวลาที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="d593c-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="d593c-106">หัวข้อนี้แสดงรายการขั้นตอนของการตั้งค่าการชำระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="d593c-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="d593c-107">การชดเชยภาษีหัก ณ ที่จ่าย (จากบัญชีลูกหนี้) จะไม่ถูกพิจารณาเมื่อมีการคํานวณการหักภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="d593c-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="d593c-108">ไปที่ **บานหน้าต่างการนำทาง > โมดูล > ภาษี > การประกาศ > ภาษีหัก ณ ที่จ่าย > การชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="d593c-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="d593c-109">ในฟิลด์ **รอบระยะเวลาการจ่ายเงิน** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="d593c-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d593c-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d593c-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d593c-111">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d593c-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="d593c-112">ในฟิลด์ **วันที่ทำธุรกรรม** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d593c-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="d593c-113">เลือก **อัปเดต** เพื่อลงรายการบัญชีใบสำคัญจ่ายภาษีหัก ณ ที่จ่ายไปยังบัญชีหักภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="d593c-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="d593c-114">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d593c-114">Click **OK**.</span></span>

![พารามิเตอร์การชำระภาษีหัก ณ ที่จ่าย](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]