---
title: ตั้งค่ารหัสการรายงานภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS
description: รหัสการรายงานภาษีหัก ณ ที่จ่ายถูกใช้ในการสร้างรายงานฟอร์ม 26Q และฟอร์ม 27Q สำหรับภาษีที่หักที่ต้นทาง (TDS) หัวข้อนี้อธิบายวิธีการตั้งค่าขั้นตอนของรหัสการรายงานภาษีหัก ณ ที่จ่าย เพื่อให้คุณสามารถตั้งค่ารหัสการรายงาน TDS ได้
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023638"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="de17e-104">ตั้งค่ารหัสการรายงานภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="de17e-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de17e-105">รหัสการรายงานภาษีหัก ณ ที่จ่ายถูกใช้ในการสร้างรายงานฟอร์ม 26Q และฟอร์ม 27Q สำหรับภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="de17e-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="de17e-106">หัวข้อนี้อธิบายวิธีการตั้งค่าขั้นตอนของรหัสการรายงานภาษีหัก ณ ที่จ่าย เพื่อให้คุณสามารถตั้งค่ารหัสการรายงาน TDS ได้</span><span class="sxs-lookup"><span data-stu-id="de17e-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="de17e-107">ไปที่ **ภาษี \> การตั้งค่า \> ภาษีหัก ณ ที่จ่าย \> รหัสการรายงานภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="de17e-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="de17e-108">[![หน้ารหัสการรายงานภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="de17e-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="de17e-109">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อกำหนดรหัสการรายงานภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="de17e-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="de17e-110">ในฟิลด์ **ส่วนประกอบภาษีหัก ณ ที่จ่าย** ให้เลือกส่วนประกอบ TDS ที่คุณต้องการระบุรหัสการรายงานภาษีหัก ณ ที่จ่ายให้</span><span class="sxs-lookup"><span data-stu-id="de17e-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="de17e-111">ฟิลด์ **กลุ่มส่วนประกอบภาษี หัก ณ ที่จ่าย** แสดงกลุ่มส่วนประกอบ TDS ที่กําหนดไว้สำหรับส่วนประกอบ TDS ที่คุณกําหนดอยู่</span><span class="sxs-lookup"><span data-stu-id="de17e-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="de17e-112">ฟิลด์ **รหัสส่วน** บน FastTab **ทั่วไป** จะแสดงรหัสส่วนที่แนบกับกลุ่มส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="de17e-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="de17e-113">บน FastTab **ทั่วไป** ในฟิลด์ **รหัสการรายงาน** ให้เลือกรหัสการรายงาน TDS:</span><span class="sxs-lookup"><span data-stu-id="de17e-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="de17e-114">TDS</span><span class="sxs-lookup"><span data-stu-id="de17e-114">TDS</span></span>
    - <span data-ttu-id="de17e-115">TDS</span><span class="sxs-lookup"><span data-stu-id="de17e-115">TCS</span></span>
    - <span data-ttu-id="de17e-116">การเก็บเงินเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="de17e-116">Surcharge</span></span>
    - <span data-ttu-id="de17e-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="de17e-117">PE\_Cess</span></span>
    - <span data-ttu-id="de17e-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="de17e-118">SHE\_Cess</span></span>

5. <span data-ttu-id="de17e-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="de17e-119">Close the page.</span></span>
