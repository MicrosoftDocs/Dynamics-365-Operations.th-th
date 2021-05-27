---
title: ตั้งค่าส่วนประกอบภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่ากลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย เช่น ค่าเช่า และผู้รับเหมา สำหรับชนิดภาษีที่หักที่ต้นทาง (TDS)
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
ms.openlocfilehash: 23124d36389b08726defbedbd1bab9a7eb43c197
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023639"
---
# <a name="set-up-withholding-tax-component-groups-for-the-tds-tax-type"></a><span data-ttu-id="babde-103">ตั้งค่าส่วนประกอบภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="babde-103">Set up withholding tax component groups for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="babde-104">หัวข้อนี้อธิบายวิธีการตั้งค่ากลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย เช่น **ค่าเช่า** และ **ผู้รับเหมา** สำหรับชนิดภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="babde-104">This topic explains how to set up withholding tax component groups, such as **Rent** and **Contractor**, for the Tax Deducted at Source (TDS) tax type.</span></span>

1. <span data-ttu-id="babde-105">ไปที่ **ภาษี \> การตั้งค่า \> ภาษีหัก ณ ที่จ่าย \> กลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="babde-105">Go to **Tax \> Setup \> Withholding tax \> Withholding tax component groups**.</span></span>

    <span data-ttu-id="babde-106">[![หน้ากลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-8.png)](./media/apac-ind-TDS-8.png)</span><span class="sxs-lookup"><span data-stu-id="babde-106">[![Withholding tax component groups page](./media/apac-ind-TDS-8.png)](./media/apac-ind-TDS-8.png)</span></span>

2. <span data-ttu-id="babde-107">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อตั้งค่ากลุ่มส่วนประกอบภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="babde-107">In the **Tax type** field, select **TDS** to set up withholding tax component groups for the TDS tax type.</span></span>
3. <span data-ttu-id="babde-108">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="babde-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="babde-109">ในฟิลด์ **กลุ่มส่วนประกอบภาษีหัก ณ ที่จ่าย** ให้ป้อนชื่อสำหรับกลุ่มส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="babde-109">In the **Withholding tax component group** field, enter a name for the TDS component group.</span></span>
5. <span data-ttu-id="babde-110">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="babde-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="babde-111">บน FastTab **ทั่วไป** ในฟิลด์ **สถานะ** ให้เลือกสถานะที่พักอาศัยของกลุ่มส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="babde-111">On the **General** FastTab, in the **Status** field, select the residential status of the TDS component group.</span></span> <span data-ttu-id="babde-112">ตัวเลือกได้แก่ **มีถิ่นที่อยู่ในประเทศ** และ **มีถิ่นที่อยู่นอกประเทศ**</span><span class="sxs-lookup"><span data-stu-id="babde-112">The options are **Resident** and **Non-resident**.</span></span>
7. <span data-ttu-id="babde-113">ในฟิลด์ **รหัสส่วน** ให้ป้อนรหัสส่วนที่ใช้กับกลุ่มส่วนประกอบ TDS</span><span class="sxs-lookup"><span data-stu-id="babde-113">In the **Section code** field, enter the section code that is applied to the TDS component group.</span></span>
8. <span data-ttu-id="babde-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="babde-114">Close the page.</span></span>
