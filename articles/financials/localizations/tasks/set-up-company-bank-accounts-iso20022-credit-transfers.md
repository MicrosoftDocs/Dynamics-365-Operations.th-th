---
title: ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการโอนย้ายเครดิต ISO20022
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงิน '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848755"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="3aa19-103">ตั้งค่าบัญชีธนาคารของบริษัทสำหรับการโอนย้ายเครดิต ISO20022</span><span class="sxs-lookup"><span data-stu-id="3aa19-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3aa19-104">กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลบัญชีธนาคารเฉพาะบริษัทที่จำเป็นสำหรับการสร้างไฟล์การชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="3aa19-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="3aa19-105">คุณตั้งค่าข้อมูลที่จำเป็นในการสร้างรูปแบบการโอนย้ายเครดิต ISO 20022 แต่ทั้งนี้ขึ้นอยู่กับรูปแบบ อาจจำเป็นต้องมีข้อมูลอื่น เช่น รหัสบริษัทหรือรหัสเรียงลำดับ </span><span class="sxs-lookup"><span data-stu-id="3aa19-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="3aa19-106">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="3aa19-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="3aa19-107">นี่คือกระบวนงานที่สองจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="3aa19-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="3aa19-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="3aa19-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="3aa19-109">ตั้งค่ารหัส IBAN และ SWIFT</span><span class="sxs-lookup"><span data-stu-id="3aa19-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="3aa19-110">ไปที่การจัดการเงินสดและธนาคาร > บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3aa19-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="3aa19-111">ใช้ตัวกรองด่วนเพื่อกรองฟิลด์บัญชีธนาคาร ด้วยค่า 'DEMF OPER'</span><span class="sxs-lookup"><span data-stu-id="3aa19-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="3aa19-112">คลิก DEMF OPER เพื่อเปิดรายละเอียดบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3aa19-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="3aa19-113">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="3aa19-113">Click Edit.</span></span>
5. <span data-ttu-id="3aa19-114">ขยายส่วนการระบุรหัสประจำตัวเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3aa19-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="3aa19-115">ในฟิลด์ IBAN ให้พิมพ์ 'DE89370400440532013000'</span><span class="sxs-lookup"><span data-stu-id="3aa19-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="3aa19-116">ในฟิลด์รหัส SWIFT ให้พิมพ์ 'DEUTDEFF'</span><span class="sxs-lookup"><span data-stu-id="3aa19-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="3aa19-117">โปรดทราบว่าไม่จำเป็นต้องใช้ SWIFT\BIC สำหรับรูปแบบการชำระเงินหลายรายการ อย่างไรก็ตาม ขอแนะนำให้ลงทะเบียนสำหรับบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3aa19-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="3aa19-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3aa19-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="3aa19-119">ตั้งค่าบัญชีธนาคารสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="3aa19-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="3aa19-120">ไปที่การจัดการองค์กร > องค์กร > นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="3aa19-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="3aa19-121">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="3aa19-121">Click Edit.</span></span>
3. <span data-ttu-id="3aa19-122">ขยายส่วนของข้อมูลบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3aa19-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="3aa19-123">ในฟิลด์บัญชีธนาคาร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3aa19-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="3aa19-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3aa19-124">Click Save.</span></span>

