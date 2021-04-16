---
title: งานการจัดการเครดิตประจำงวด
description: หัวข้อนี้อธิบายงานประจำงวดที่เป็นส่วนหนึ่งที่จำเป็นในการจัดการวงเงินสินเชื่อสำหรับลูกค้า
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e5d1ad7b0b151d67bd96513e9ce0c82c172a601
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835303"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="6e0d7-103">งานการจัดการสินเชื่อประจำงวด</span><span class="sxs-lookup"><span data-stu-id="6e0d7-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e0d7-104">หัวข้อนี้อธิบายงานประจำงวดที่เป็นส่วนหนึ่งที่จำเป็นในการจัดการวงเงินสินเชื่อสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6e0d7-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="6e0d7-105">อัพเดตคะแนนความเสี่ยง</span><span class="sxs-lookup"><span data-stu-id="6e0d7-105">Update risk scores</span></span>

<span data-ttu-id="6e0d7-106">ในขณะที่ธุรกิจพัฒนาและสถานการณ์เปลี่ยนแปลง ความเสี่ยงด้านเครดิตสำหรับลูกค้าที่กำหนดก็สามารถเปลี่ยนแปลงได้เช่นกัน</span><span class="sxs-lookup"><span data-stu-id="6e0d7-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="6e0d7-107">เมื่อต้องการรักษาวงเงินสินเชื่อที่เหมาะสมสำหรับลูกค้าของคุณ คุณต้องตรวจทานเงื่อนไขสำหรับคะแนนความเสี่ยงแต่ละรายการเป็นครั้งคราว และปรับปรุงคะแนนสำหรับลูกค้าแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="6e0d7-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="6e0d7-108">คุณสามารถปรับปรุงคะแนนต่อไปนี้ได้โดยใช้หน้า **ปรับปรุงคะแนนความเสี่ยง** (**สินเชื่อและการเรียกเก็บเงิน \> งานประจำงวด \> การจัดการเครดิต \> ปรับปรุงคะแนนความเสี่ยง**)</span><span class="sxs-lookup"><span data-stu-id="6e0d7-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="6e0d7-109">นอกจากนี้ การคำนวณที่กำหนดโดยผู้ใช้ทั้งหมดจะได้รับการประมวลผลด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="6e0d7-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="6e0d7-110">**จำนวนวันการชำระเงินเฉลี่ย** – คะแนนนี้คือจำนวนวันเฉลี่ยที่ลูกค้าใช้ในการชำระเงินตามใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="6e0d7-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="6e0d7-111">**ลูกค้าตั้งแต่** – คะแนนนี้เป็นจำนวนปีที่ลูกค้าเป็นลูกค้าขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="6e0d7-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="6e0d7-112">**ในธุรกิจตั้งแต่** – คะแนนนี้เป็นจำนวนปีที่ลูกค้าอยู่ในธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="6e0d7-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="6e0d7-113">ซึ่งใช้ค่าของฟิลด์ **การเริ่มต้นของธุรกิจ** ในหน้า **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="6e0d7-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="6e0d7-114">**ระยะเวลาการเก็บหนี้ถัวเฉลี่ย** – คะแนนนี้จะขึ้นอยู่กับยอดดุลบัญชีลูกหนี้ รายได้จากการขาย และจำนวนวันสำหรับรอบระยะเวลา 12 เดือนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6e0d7-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="6e0d7-115">**ยอดดุลเฉลี่ย** – คะแนนนี้จะขึ้นอยู่กับยอดดุลบัญชีลูกหนี้สำหรับรอบระยะเวลา 12 เดือนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="6e0d7-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="6e0d7-116">**กลุ่มการจัดการเครดิต** **สถานะของบัญชี** และ **ประเทศ** – คะแนนเหล่านี้จะใช้ข้อมูลจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6e0d7-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="6e0d7-117">ปรับปรุงสถิติยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6e0d7-117">Update customer balance statistics</span></span>

<span data-ttu-id="6e0d7-118">คุณสามารถรันกระบวนการ **ปรับปรุงสถิติยอดดุลของลูกค้า** เพื่อปรับปรุงการคำนวณสถิติยอดดุลที่แสดงบนหน้า **การสอบถามเกี่ยวกับสถิติยอดดุล**</span><span class="sxs-lookup"><span data-stu-id="6e0d7-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="6e0d7-119">ข้อมูลนี้จะใช้ในการคำนวณคะแนนความเสี่ยงและค่าที่แสดงในกล่องแสดงข้อมูลย่อสถิติเครดิตบนหน้า **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="6e0d7-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="6e0d7-120">เมื่อคุณรันกระบวนการ จะปรับปรุงสถิติยอดดุลของลูกค้าสำหรับลูกค้ารายเดียว</span><span class="sxs-lookup"><span data-stu-id="6e0d7-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="6e0d7-121">เมื่อต้องการตั้งค่าชุดงานเพื่อรันกระบวนการสำหรับลูกค้าหลายราย คุณสามารถใช้หน้า **คำนวณสถิติยอดดุล** (**การจัดการเครดิต \> งานประจำงวด \> คำนวณสถิติยอดดุล**)</span><span class="sxs-lookup"><span data-stu-id="6e0d7-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]