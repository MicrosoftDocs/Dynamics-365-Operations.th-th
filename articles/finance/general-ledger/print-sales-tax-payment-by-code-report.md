---
title: พิมพ์รายงานการชำระภาษีขายโดยเรียงตามรหัส
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับการตั้งค่าและการดำเนินการที่จำเป็นในการพิมพ์รายงานการชำระภาษีขาย โดยเรียงตามรหัสในสกุลเงินทางบัญชีหรือรหัสภาษี
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815463"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="3c31d-103">พิมพ์รายงานการชำระภาษีขายโดยเรียงตามรหัส</span><span class="sxs-lookup"><span data-stu-id="3c31d-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c31d-104">เมื่อต้องการพิมพ์รายงาน **การชำระภาษีขายโดยเรียงตามรหัส** ให้ไปที่ **ภาษี** \> **การสอบถามและรายงาน** \> **รายงานภาษีขาย** \> **การชำระภาษีขายโดยเรียงตามรหัส**</span><span class="sxs-lookup"><span data-stu-id="3c31d-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="3c31d-105">โดยค่าเริ่มต้น จะมีการสร้างยอดเงินรายงานในสกุลเงินทางบัญชีของนิติบุคคลสำหรับรหัสการรายงานทั้งหมดที่ตั้งค่าไว้ในหน้า **รหัสการรายงานภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="3c31d-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="3c31d-106">นอกจากนี้ คุณยังสามารถสร้างรายงานนี้เพื่อให้แสดงยอดเงินการชำระภาษีขายในสกุลเงินของรหัสภาษีขาย สำหรับรหัสการรายงานทั้งหมดที่กำหนดให้กับรหัสภาษีขายในหน้า **รหัสภาษีขาย** ได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="3c31d-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="3c31d-107">เปิดคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="3c31d-107">Turn on the feature</span></span>

<span data-ttu-id="3c31d-108">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เปิดใช้งานคุณลักษณะต่อไปนี้: **สร้างรายงานการชำระภาษีขายตามรหัสในสกุลเงินรหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="3c31d-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="3c31d-109">รันรายงาน</span><span class="sxs-lookup"><span data-stu-id="3c31d-109">Run the report</span></span>

1. <span data-ttu-id="3c31d-110">ไปที่ **ภาษี** \> **การสอบถามและรายงาน** \> **รายงานภาษีขาย** \> **การชำระภาษีขายตามรหัส**</span><span class="sxs-lookup"><span data-stu-id="3c31d-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="3c31d-111">ในฟิลด์ **สกุลเงินการรายงาน** เลือกหนึ่งในค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3c31d-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="3c31d-112">**สกุลเงินทางบัญชี** – พิมพ์ยอดเงินรายงานในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="3c31d-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="3c31d-113">**สกุลเงินรหัสภาษีขาย** – พิมพ์ยอดเงินรายงานในสกุลเงินของรหัสภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3c31d-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![กล่องโต้ตอบการชำระภาษีขายโดยเรียงตามรหัส](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="3c31d-115">ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายงานที่ถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="3c31d-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="3c31d-116">รายงานแสดงให้เห็นว่ารหัสการรายงาน **101** มีสกุลเงิน **EUR** ถ้าฟิลด์ **สกุลเงินภาษีขาย** ถูกตั้งค่าเป็น **EUR** สำหรับรหัสภาษีขายที่มีการกำหนดรหัสการรายงาน</span><span class="sxs-lookup"><span data-stu-id="3c31d-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![ตัวอย่างของรายงานการชำระภาษีขายโดยเรียงตามรหัส](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]