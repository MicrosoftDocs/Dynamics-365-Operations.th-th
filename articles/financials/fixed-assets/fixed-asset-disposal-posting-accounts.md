---
title: "บัญชีการลงรายการการตัดจำหน่ายสินทรัพย์ถาวร"
description: "บทความนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภททั่วไปที่ลงรายการบัญชีสำหรับการตัดจำหน่ายสินทรัพย์"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: th-th
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="468df-103">บัญชีการลงรายการการตัดจำหน่ายสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="468df-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="468df-104">บทความนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภททั่วไปที่ลงรายการบัญชีสำหรับการตัดจำหน่ายสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="468df-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="468df-105">ในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวรบนแท็บด่วนบัญชีแยกประเภท ให้เลือกการตัดจำหน่าย - การขายและการตัดจำหน่าย - ของเสีย เพื่อตั้งค่าการลงรายการบัญชีในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="468df-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="468df-106">สำหรับทั้งสองชนิดธุรกรรม บัญชีแยกประเภทจะถูกเครดิตสำหรับมูลค่าการตัดจำหน่ายของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="468df-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="468df-107">มีการลงรายการบัญชีเดบิตไปยังบัญชีตรงข้าม ซึ่งอาจเป็น ตัวอย่างเช่น บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="468df-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="468df-108">ถ้าสินทรัพย์ถาวรถูกขายให้กับลูกค้า จะมีการใช้บัญชีลูกค้าแทนที่บัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="468df-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="468df-109">คลิกการตัดจำหน่าย และจากนั้นคลิกการขายหรือเศษซาก และจากนั้นตั้งค่ารายละเอียดของบัญชีเพื่อกลับรายการมูลค่าตามบัญชีสุทธิของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="468df-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="468df-110">คุณยังสามารถป้อนข้อมูลในฟิลด์มูลค่าการลงรายการบัญชีและมูลค่าการขาย ในหน้าพารามิเตอร์การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="468df-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="468df-111">ธุรกรรมการตัดจำหน่ายสำหรับสินทรัพย์ในกลุ่มสินทรัพย์มูลค่าต่ำ ลดมูลค่าตามบัญชีสุทธิของกลุ่มสินทรัพย์มูลค่าต่ำตามยอดเงินที่ตัดจำหน่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="468df-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="468df-112">อย่างไรก็ตาม เมื่อการขายสินทรัพย์นั้นเกินมูลค่าตามบัญชีสุทธิของกลุ่มสินทรัพย์มูลค่าต่ำ มูลค่าตามบัญชีสุทธิจะถูกลดลงเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="468df-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






