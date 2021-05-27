---
title: ตั้งค่าพารามิเตอร์ TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์เพื่อเรียกใช้ฟังก์ชันภาษีที่หักที่ต้นทาง (TDS) ในธุรกรรมที่ระบุ นี่เป็นขั้นตอนที่จําเป็นในการใช้คุณลักษณะภาษีที่หักที่ต้นทาง TDS
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023626"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="4af55-104">ตั้งค่าพารามิเตอร์ TDS</span><span class="sxs-lookup"><span data-stu-id="4af55-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4af55-105">หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์เพื่อเรียกใช้ฟังก์ชันภาษีที่หักที่ต้นทาง (TDS) ในธุรกรรมที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="4af55-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="4af55-106">นี่เป็นขั้นตอนที่จําเป็นในการใช้คุณลักษณะภาษีที่หักที่ต้นทาง TDS</span><span class="sxs-lookup"><span data-stu-id="4af55-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="4af55-107">ไปที่ **บัญชีแยกประเภททั่วไปr \> การตั้งค่าบัญชีแยกประเภท \>พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="4af55-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="4af55-108">บนแท็บ **ภาษีทางตรง** ในส่วน **ภาษีที่หักที่ต้นทาง** ให้ตั้งค่าตัวเลือก **เรียกใช้ TDS** เป็น **ใช่** เพื่อเรียกใช้ฟังก์ชันTDS และหน้าและฟิลด์ที่ถูกใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="4af55-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="4af55-109">ตั้งค่าตัวเลือก **ใบแจ้งหนี้** เป็น **ใช่** เพื่อเรียกใช้ฟิลด์ที่ใช้ในการคํานวณและหัก TDS ในระดับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4af55-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="4af55-110">ตั้งค่าตัวเลือก **การชำระเงิน** เป็น **ใช่** เพื่อเรียกใช้ฟิลด์ที่ใช้ในการคํานวณและหัก TDS ในระดับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4af55-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="4af55-111">[![แท็บภาษีทางตรง](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="4af55-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="4af55-112">บนแท็บ **ลำดับหมายเลข** ให้ค้นหาแถวที่มีการตั้งค่าฟิลด์ **ข้อมูลอ้างอิง** เป็น **การชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="4af55-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="4af55-113">ในฟิลด์ **รหัสลำดับหมายเลข** สำหรับแถว ให้เลือกรหัสลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4af55-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="4af55-114">รหัสลำดับหมายเลขนี้ถูกใช้ในการสร้างหมายเลขใบสำคัญสำหรับกระบวนการชําระเงิน TDS ประจำงวด</span><span class="sxs-lookup"><span data-stu-id="4af55-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4af55-115">เมื่อต้องการรันกระบวนการชําระเงิน TDS ประจำงวด ให้ไปที่ **ภาษี \>  ประกาศต่างๆ \> ภาษีหัก ณ ที่จ่าย \> การชำระภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="4af55-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="4af55-116">[![แท็บลำดับหมายเลข](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="4af55-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="4af55-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4af55-117">Close the page.</span></span>
