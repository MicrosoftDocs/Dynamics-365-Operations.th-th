---
title: ตั้งค่านามแฝงของบัญชีแยกประเภท
description: 'ขั้นตอนนี้แสดงวิธีการสร้างนามแฝงของบัญชีที่มีทางลัดสำหรับการป้อนหมายเลขบัญชี '
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccountAlias
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2098ffed81ab3c18855363f0c3ef43dc1d11a77d
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138103"
---
# <a name="set-up-a-ledger-account-alias"></a><span data-ttu-id="782da-103">ตั้งค่านามแฝงของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="782da-103">Set up a ledger account alias</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="782da-104">ขั้นตอนนี้แสดงวิธีการสร้างนามแฝงของบัญชีที่มีทางลัดสำหรับการป้อนหมายเลขบัญชี </span><span class="sxs-lookup"><span data-stu-id="782da-104">This procedure shows how to create an account alias that provides a shortcut for entering an account number.</span></span> <span data-ttu-id="782da-105">ผู้ใช้ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="782da-105">This procedure users demo data company USMF.</span></span>

1. <span data-ttu-id="782da-106">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > นามแฝงของบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="782da-106">Go to General ledger > Chart of accounts > Accounts > Ledger account alias.</span></span>
2. <span data-ttu-id="782da-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="782da-107">Click New.</span></span>
3. <span data-ttu-id="782da-108">ในฟิลด์นามแฝงของบัญชีแยกประเภท ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="782da-108">In the Ledger account alias field, type a value.</span></span>
4. <span data-ttu-id="782da-109">ในฟิลด์โครงสร้างทางบัญชี เลือกโครงสร้างที่เป็นของบัญชีและมิติ</span><span class="sxs-lookup"><span data-stu-id="782da-109">In the Account structure field, select the structure the account and dimensions belong to.</span></span>
5. <span data-ttu-id="782da-110">ในฟิลด์บริษัท ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="782da-110">In the Company field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="782da-111">ในรายการนี้ ให้หาและเลือกบริษัทที่จะนำนามแฝงไปใช้</span><span class="sxs-lookup"><span data-stu-id="782da-111">In the list, find and select the company that the alias applies to.</span></span>
7. <span data-ttu-id="782da-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="782da-112">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="782da-113">ในฟิลด์ข้อกำหนดนามแฝงของบัญชีแยกประเภท ให้ระบุบัญชีและมิติ</span><span class="sxs-lookup"><span data-stu-id="782da-113">In the Ledger account alias definition field, specify the account and dimensions.</span></span>
    * <span data-ttu-id="782da-114">บัญชีและมิติจะถูกเติมเมื่อใช้ทางลัด</span><span class="sxs-lookup"><span data-stu-id="782da-114">The account and dimensions will be populated when using the shortcut.</span></span>  
9. <span data-ttu-id="782da-115">ในฟิลด์โฟกัสเริ่มต้น ให้เลือกมิติที่จะมีโฟกัสเมื่อนามแฝงถูกใช้</span><span class="sxs-lookup"><span data-stu-id="782da-115">In the Initial focus field, select the dimension that will have focus when the alias is used.</span></span>
    * <span data-ttu-id="782da-116">หลังจากที่คุณพิมพ์ลัด และเติมข้อมูลบัญชีและมิติ ฟิลด์โฟกัสเริ่มต้นคือ ตำแหน่งที่เคอร์เซอร์หรือโฟกัสย้ายไป</span><span class="sxs-lookup"><span data-stu-id="782da-116">After you type the shortcut, and the account and dimensions are populated, the Initial focus field is where the cursor or focus will move to.</span></span>  

