---
title: ตั้งค่าข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ SEPA
description: ระบบการชำระเงินของสหภาพยุโรป (SEPA) การหักบัญชีเงินฝากอัตโนมัติช่วยให้เจ้าหนี้เรียกเก็บเงินจากบัญชีธนาคารของลูกค้า ได้รับว่าลูกค้าได้อนุญาตให้มีการลงชื่อข้อตกลงกับเจ้าหนี้
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24803e7157edc87e73eb6c8af404311bdf8fc5c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245627"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="a1f9f-103">ตั้งค่าข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ SEPA</span><span class="sxs-lookup"><span data-stu-id="a1f9f-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1f9f-104">ระบบการชำระเงินของสหภาพยุโรป (SEPA) การหักบัญชีเงินฝากอัตโนมัติช่วยให้เจ้าหนี้เรียกเก็บเงินจากบัญชีธนาคารของลูกค้า ได้รับว่าลูกค้าได้อนุญาตให้มีการลงชื่อข้อตกลงกับเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="a1f9f-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="a1f9f-105">ข้อตกลงที่ลูกค้าลงชื่ออนุมัติเจ้าหนี้เพื่อรวบรวมการชำระเงินและสั่งให้ธนาคารของลูกค้าชำระใบเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="a1f9f-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="a1f9f-106">หัวข้อนี้มีการจัดระเบียบเพื่อแสดงกระบวนการสำหรับการตั้งค่าข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ SEPA</span><span class="sxs-lookup"><span data-stu-id="a1f9f-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a1f9f-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a1f9f-107">Prerequisites</span></span>
<span data-ttu-id="a1f9f-108">ตารางต่อไปนี้แสดงข้อกำหนดเบื้องต้นที่ต้องมีก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a1f9f-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="a1f9f-109">ประเภท</span><span class="sxs-lookup"><span data-stu-id="a1f9f-109">Category</span></span>       | <span data-ttu-id="a1f9f-110">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="a1f9f-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f9f-111">ประเทศ/ภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="a1f9f-111">Country/region</span></span> | <span data-ttu-id="a1f9f-112">ที่อยู่หลักสำหรับนิติบุคคลต้องอยู่ในประเทศ/ภูมิภาคดังต่อไปนี้: ออสเตรีย เบลเยียม เยอรมนี สเปน ฝรั่งเศส อิตาลี หรือเนเธอร์แลนด์</span><span class="sxs-lookup"><span data-stu-id="a1f9f-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="a1f9f-113">ตั้งค่าลำดับหมายเลขสำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ ข้อตกลงแต่ละเดบิตโดยตรงต้องมีหมายเลขเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="a1f9f-114">ใช้หน้า **ลำดับหมายเลข** เพื่อสร้างลำดับหมายเลขสำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="a1f9f-115">คุณจะใช้ตัวระบุนี้เพื่อกำหนดลำดับหมายเลขไปยังระบบข้อตกลงการหักบัญชีเงินฝากอัตโนมัติในหน้า **พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="a1f9f-116">ตั้งค่าพารามิเตอร์บัญชีลูกหนี้สำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ ใช้หน้า **พารามิเตอร์บัญชีลูกหนี้** เพื่อตั้งค่าพารามิเตอร์สำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="a1f9f-117">เมื่อต้องการตั้งค่าพารามิเตอร์ บนแท็บ **การหักบัญชีเงินฝากอัตโนมัติ** เปลี่ยนพารามิเตอร์เริ่มต้นตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="a1f9f-118">จากนั้นบนแท็บ **ลำดับหมายเลข** อัพเดตฟิลด์ **รหัสข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ** ด้วยลำดับหมายเลขที่คุณติดตั้งก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="a1f9f-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="a1f9f-119">ตั้งค่าวิธีการชำระเงินสำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ คุณต้องตั้งค่าวิธีการชำระเงินสำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="a1f9f-120">คุณใช้วิธีการชำระเงินเพื่อการสอบถามสำหรับใบแจ้งหนี้เพื่อสร้างการชำระเงินการหักบัญชีเงินฝากอัตโนมัติสำหรับ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="a1f9f-121">ใช้หน้า **วิธีการชำระเงิน** เพื่อตั้งค่าวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="a1f9f-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="a1f9f-122">การตั้งค่าวิธีการชำระเงินสำหรับข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ คุณต้องทำตามขั้นตอนเพิ่มเติมเหล่านี้สำหรับวิธีการชำระเงิน:</span><span class="sxs-lookup"><span data-stu-id="a1f9f-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="a1f9f-123">ในฟิลด์ **ชนิดการชำระเงิน** เลือก **การชำระเงินทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="a1f9f-124">ไม่จำเป็นต้องระบุ: ถ้าคุณคาดว่าลูกค้าของคุณแต่ละคนมีข้อบังคับหลายรายการ ในฟิลด์ **รอบระยะเวลา** เลือก **ใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="a1f9f-125">การชำระเงินจะถูกสร้างแยกต่างหากสำหรับแต่ละใบแจ้งหนี้และการชำระเงินแต่ละรายการจะใช้ข้อตกลงที่ระบุไว้สำหรับใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="a1f9f-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="a1f9f-126">เลือกตัวเลือก **ต้องใช้ข้อตกลง** เพื่อสร้างการชำระเงินโดยการใช้ข้อตกลงการหักบัญชีเงินฝากอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a1f9f-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="a1f9f-127">ตัวเลือก **ต้องใช้ข้อตกลง** จะพร้อมใช้งานได้เมื่อคุณเลือกเท่านั้น **ชำระเงินทางอิเล็กทรอนิกส์** ในฟิลด์ **ชนิดการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="a1f9f-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="a1f9f-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a1f9f-128">Additional resources</span></span>

[<span data-ttu-id="a1f9f-129">ภาพรวมการหักบัญชีเงินฝากอัตโนมัติ SEPA</span><span class="sxs-lookup"><span data-stu-id="a1f9f-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="a1f9f-130">สร้างข้อตกลงการหักบัญชีเงินฝากอัตโนมัติสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="a1f9f-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]