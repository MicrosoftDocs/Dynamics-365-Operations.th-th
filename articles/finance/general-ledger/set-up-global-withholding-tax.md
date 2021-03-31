---
title: ตั้งค่าภาษีหัก ณ ที่จ่ายส่วนกลาง
description: หัวข้อนี้แสดงรายการขั้นตอนต่างๆ ของการตั้งค่าภาษีหัก ณ ที่จ่ายสากลเกี่ยวกับการขายและการซื้อ
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
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204844"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="5fa1b-103">ตั้งค่าภาษีหัก ณ ที่จ่ายส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="5fa1b-103">Set up global withholding tax</span></span>

<span data-ttu-id="5fa1b-104">หัวข้อนี้แสดงรายการขั้นตอนต่างๆ ของการตั้งค่าภาษีหัก ณ ที่จ่ายสากลเกี่ยวกับการขายและการซื้อ</span><span class="sxs-lookup"><span data-stu-id="5fa1b-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="5fa1b-105">ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายบนหน้า **หน่วยจัดเก็บภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="5fa1b-106">ตั้งค่าการหัก ณ ที่จ่ายของรอบระยะเวลาการชำระเงินบนหน้า **รอบระยะเวลาการชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="5fa1b-107">ตั้งค่ากลุ่มการลงรายการบัญชีแยกประเภทภาษีหัก ณ ที่จ่ายในหน้า **ภาษีหัก ณ ที่จ่าย > กลุ่มการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="5fa1b-108">**ภาษีหัก ณ ที่จ่าย** จะถูกมอบหมายด้วยบัญชีหลักที่มี **ชนิดการลงรายการบัญชี** ภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="5fa1b-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="5fa1b-109">**การชดเชยภาษีหัก ณ ที่จ่าย** จะถูกมอบหมายด้วยบัญชีหลักที่มี **ชนิดการลงรายการบัญชี** การชดเชยภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="5fa1b-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="5fa1b-110">ไปที่ **บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > บัญชีหลัก** ตั้งค่า **ชนิดการลงรายการบัญชี** ในฟอร์มย่อย **การตรวจสอบความถูกต้องของการลงรายการบัญชี** สำหรับบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="5fa1b-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="5fa1b-111">ตั้งค่ารหัสภาษีหัก ณ ที่จ่ายบนหน้า **รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="5fa1b-112">ตั้งค่ากลุ่มภาษีหัก ณ ที่จ่ายบนหน้า **กลุ่มภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="5fa1b-113">ตั้งค่าประเภทรายได้ที่ต้องเสียภาษีหัก ณ ที่จ่ายบนหน้า **ประเภท** **รายได้ที่ต้องเสียภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="5fa1b-114">ตั้งค่ากลุ่มภาษีหัก ณ ที่จ่ายบนหน้า **กลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้า** สำหรับสินค้าหรือบริการ</span><span class="sxs-lookup"><span data-stu-id="5fa1b-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="5fa1b-115">ตั้งค่า **จำนวนในใบแจ้งหนี้ขั้นต่ำ** ในหน้า **พารามิเตอร์บัญชีแยกประเภททั่วไป > หน้าภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="5fa1b-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]