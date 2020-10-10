---
title: เลตเตอร์ออฟเครดิต
description: เลตเตอร์ออฟเครดิตมีเอกสารธนาคารที่ใช้สำหรับการซื้อและการขายสินค้าข้ามพรมแดนประเทศ
author: panolte
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLCImport
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 18271
ms.assetid: aa594beb-bdb2-4117-91c2-d097d9401b0f
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a9be6ad2ff90dffdf8548d7594f922a7cf9b404
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899432"
---
# <a name="letters-of-credit"></a><span data-ttu-id="337cb-103">เลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-103">Letters of credit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="337cb-104">เลตเตอร์ออฟเครดิตมีเอกสารธนาคารที่ใช้สำหรับการซื้อและการขายสินค้าข้ามพรมแดนประเทศ</span><span class="sxs-lookup"><span data-stu-id="337cb-104">Letters of credit are bank documents that are commonly used for the purchase and sale of goods across international borders.</span></span> 

<span data-ttu-id="337cb-105">เลตเตอร์ออฟเครดิตจะใช้สำหรับธุรกรรมระหว่างประเทศเพื่อให้แน่ใจว่าการชำระเงินเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="337cb-105">Letters of credit are used for international transactions to ensure that payments will be made.</span></span> <span data-ttu-id="337cb-106">เลตเตอร์ออฟเครดิตคือ ข้อตกลงที่ออก โดยธนาคาร ที่ธนาคารตกลงเพื่อให้แน่ใจว่าการชำระเงินในนามของผู้ซื้อ ว่าตรงตามเงื่อนไขของข้อตกลงระหว่างผู้ซื้อและผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="337cb-106">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span> <span data-ttu-id="337cb-107">โปรดทราบว่า เลตเตอร์ออฟเครดิตยังถือเป็นเครดิต (DC) มีเอกสารประกอบ</span><span class="sxs-lookup"><span data-stu-id="337cb-107">Note that a letter of credit is also referred to as a documentary credit (DC).</span></span> 

<span data-ttu-id="337cb-108">สำหรับการนำเข้าเลตเตอร์ออฟเครดิต นิติบุคคลเป็นผู้ซื้อหรือผู้สมัครสำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-108">For an import letter of credit, the legal entity is the buyer or the applicant for the letter of credit.</span></span> <span data-ttu-id="337cb-109">สำหรับการส่งออกเลตเตอร์ออฟเครดิต นิติบุคคลเป็นผู้ขายหรือผู้รับผลประโยชน์สำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-109">For an export letter of credit, the legal entity is the seller or the beneficiary of the letter of credit.</span></span> <span data-ttu-id="337cb-110">ฝ่ายต่าง ๆ ต่อไปนี้เกี่ยวข้องกับเลตเตอร์ออฟเครดิต:</span><span class="sxs-lookup"><span data-stu-id="337cb-110">The following parties are involved with a letter of credit:</span></span> 

 - <span data-ttu-id="337cb-111">ผู้สมัคร (ผู้ซื้อ) ที่ต้องการชำระเงินสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="337cb-111">The applicant (buyer) who intends to pay for the goods</span></span> 
 - <span data-ttu-id="337cb-112">ผู้รับผลประโยชน์ (ผู้ขาย) ที่จะได้รับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="337cb-112">The beneficiary (seller) who will receive the payment</span></span>
 - <span data-ttu-id="337cb-113">ธนาคารผู้ออกที่ออกเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-113">The issuing bank that issues the letter of credit</span></span>
 - <span data-ttu-id="337cb-114">ธนาคารผู้แจ้งเครดิตที่ทำธุรกรรมในนามของผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="337cb-114">The advising bank that carries out the transaction on behalf of the applicant</span></span>

<span data-ttu-id="337cb-115">เลตเตอร์ออฟเครดิตมีคำอธิบายของสินค้า ใด ๆ ที่จำเป็นต้องใช้เอกสาร วันของการจัดส่ง และวันหมดอายุหลังจากการชำระเงินจะไม่สามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="337cb-115">The letter of credit includes a description of the goods, any required documents, the date of shipment, and the expiration date after which payment will not be made.</span></span> <span data-ttu-id="337cb-116">การออกเอกสารธนาคารรวบรวมกำไรขั้นต้นสำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-116">The issuing bank collects a margin for the letter of credit.</span></span> 

<span data-ttu-id="337cb-117">เลตเตอร์ออฟเครดิตสามารถถูกเพิกถอนหรือไม่เพิกถอนก็ได้</span><span class="sxs-lookup"><span data-stu-id="337cb-117">A letter of credit can be revocable or irrevocable.</span></span> <span data-ttu-id="337cb-118">ลักษณะของเลตเตอร์ออฟเครดิตสามารถโอนย้ายได้ ไม่สามารถโอนย้ายได้ หรือหมุนเวียน</span><span class="sxs-lookup"><span data-stu-id="337cb-118">The nature of a letter of credit can be transferable, non transferable, or revolving.</span></span> <span data-ttu-id="337cb-119">โดยทั่วไป เลตเตอร์ออฟเครดิตคือการเพิกถอนไม่ได้ และยืนยันข้อตกลงที่จะทำการชำระเงินกับผู้รับผลประโยชน์เฉพาะเมื่อมีการส่งเอกสารการจัดส่งสินค้าเสร็จสมบูรณ์ และถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="337cb-119">Typically, a letter of credit is an irrevocable and confirmed agreement that payment will be made to a specific beneficiary upon submission of complete and accurate shipping documentation.</span></span>

<span data-ttu-id="337cb-120">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="337cb-120">For more information, see the following topics:</span></span>

[<span data-ttu-id="337cb-121">นำเข้าเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-121">Import letter of credit</span></span>](tasks/import-letter-credit.md)

[<span data-ttu-id="337cb-122">เลตเตอร์ออฟเครดิตสำหรับการส่งออก</span><span class="sxs-lookup"><span data-stu-id="337cb-122">Export letter of credit</span></span>](tasks/export-letter-credit.md)

[<span data-ttu-id="337cb-123">สร้างข้อตกลงสินเชื่อธนาคารสำหรับเลตเตอร์ออฟเครดิต</span><span class="sxs-lookup"><span data-stu-id="337cb-123">Create a bank facility agreement for a letter of credit</span></span>](tasks/create-bank-facility-agreement-letter-credit.md)


