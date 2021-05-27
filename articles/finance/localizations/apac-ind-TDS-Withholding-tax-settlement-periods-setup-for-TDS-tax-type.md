---
title: ตั้งค่ารหัสรอบระยะเวลาการชำระภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่ารอบระยะเวลาการชำระเงินสำหรับระยะเวลาการชำระเงินของภาษีที่หักที่ต้นทาง (TDS)
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023615"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="62816-103">ตั้งค่ารหัสรอบระยะเวลาการชำระภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="62816-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62816-104">หัวข้อนี้อธิบายวิธีการตั้งค่ารอบระยะเวลาการชำระเงินสำหรับระยะเวลาการชำระเงินของภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="62816-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="62816-105">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> ระยะเวลาการชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="62816-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="62816-106">[![หน้ารอบระยะเวลาการชำระภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="62816-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="62816-107">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อตั้งค่ารอบระยะเวลาการชำระภาษีหัก ณ ที่จ่ายให้กับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="62816-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="62816-108">เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="62816-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="62816-109">ในฟิลด์ **รอบระยะเวลาการชำระเงิน** ให้ป้อนชื่อสำหรับรอบระยะเวลาการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="62816-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="62816-110">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="62816-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="62816-111">ในฟิลด์ **หน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย** ให้เลือกหน่วยงาน TDS ที่คุณกำหนดรอบระยะเวลาการชําระเงิน TDS ให้</span><span class="sxs-lookup"><span data-stu-id="62816-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="62816-112">บน FastTab **ทั่วไป** ในฟิลด์ **ช่วงรอบระยะเวลา** ให้เลือกชนิดของช่วงรอบระยะเวลาสำหรับรอบระยะเวลาการชําระเงิน TDS</span><span class="sxs-lookup"><span data-stu-id="62816-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="62816-113">ในฟิลด์ **จํานวนของหน่วย** ให้ระบุจํานวนของหน่วยสำหรับชนิดช่วงรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="62816-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="62816-114">บน FastTab **รอบระยะเวลา** ในฟิลด์ **วันที่เริ่มต้น** ให้เลือกวันที่เริ่มต้นสำหรับรอบระยะเวลาการชําระเงิน TDS</span><span class="sxs-lookup"><span data-stu-id="62816-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="62816-115">ในฟิลด์ **วันที่สิ้นสุด** ให้เลือกวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="62816-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="62816-116">เมื่อต้องการสร้างรอบระยะเวลาการชำระเงิน TDS ในเวลาต่อมาสำหรับรอบระยะเวลาที่มีอยู่ ตามช่วงรอบระยะเวลาและหน่วยรอบระยะเวลา ให้เลือก **รอบระยะเวลาใหม่**</span><span class="sxs-lookup"><span data-stu-id="62816-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="62816-117">เมื่อต้องการดูรายละเอียดของการชําระเงิน TDS ประจำงวดที่รันสำหรับรอบระยะเวลาการชําระเงินที่ระบุ ให้เลือก **การชําระภาษีหัก ณ ที่จ่าย** เพื่อเปิดหน้า **การชําระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="62816-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="62816-118">เมื่อต้องการรันกระบวนการชําระเงิน TDS ประจำงวด ให้ไปที่ **บัญชีแยกประเภททั่วไป \> ประจำงวด \> ภาษีหัก ณ ที่จ่าย \> การชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="62816-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="62816-119">[![หน้าการชำระภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="62816-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="62816-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="62816-120">Close the page.</span></span>
