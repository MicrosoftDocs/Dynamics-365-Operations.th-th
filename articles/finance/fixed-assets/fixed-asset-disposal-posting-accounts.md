---
title: บัญชีการลงรายการการตัดจำหน่ายสินทรัพย์ถาวร
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการลงรายการบัญชีของบัญชีแยกประเภททั่วไปสำหรับการตัดจำหน่ายสินทรัพย์
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a46125dbe5262ba388e3958ea452975a98243f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187164"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="aa2be-103">บัญชีการลงรายการการตัดจำหน่ายสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="aa2be-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa2be-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการลงรายการบัญชีของบัญชีแยกประเภททั่วไปสำหรับการตัดจำหน่ายสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="aa2be-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="aa2be-105">ในหน้าโพรไฟล์การลงรายการบัญชีสินทรัพย์ถาวรบนแท็บด่วนบัญชีแยกประเภท ให้เลือกการตัดจำหน่าย - การขายและการตัดจำหน่าย - ของเสีย เพื่อตั้งค่าการลงรายการบัญชีในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="aa2be-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="aa2be-106">สำหรับทั้งสองชนิดธุรกรรม บัญชีแยกประเภทจะถูกเครดิตสำหรับมูลค่าการตัดจำหน่ายของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="aa2be-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="aa2be-107">มีการลงรายการบัญชีเดบิตไปยังบัญชีตรงข้าม ซึ่งอาจเป็น ตัวอย่างเช่น บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="aa2be-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="aa2be-108">ถ้าสินทรัพย์ถาวรถูกขายให้กับลูกค้า จะมีการใช้บัญชีลูกค้าแทนที่บัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="aa2be-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="aa2be-109">คลิกการตัดจำหน่าย และจากนั้นคลิกการขายหรือเศษซาก และจากนั้นตั้งค่ารายละเอียดของบัญชีเพื่อกลับรายการมูลค่าตามบัญชีสุทธิของสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="aa2be-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="aa2be-110">คุณยังสามารถป้อนข้อมูลในฟิลด์มูลค่าการลงรายการบัญชีและมูลค่าการขาย ในหน้าพารามิเตอร์การตัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="aa2be-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="aa2be-111">ธุรกรรมการตัดจำหน่ายสำหรับสินทรัพย์ในกลุ่มสินทรัพย์มูลค่าต่ำ ลดมูลค่าตามบัญชีสุทธิของกลุ่มสินทรัพย์มูลค่าต่ำตามยอดเงินที่ตัดจำหน่ายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="aa2be-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="aa2be-112">อย่างไรก็ตาม เมื่อการขายสินทรัพย์นั้นเกินมูลค่าตามบัญชีสุทธิของกลุ่มสินทรัพย์มูลค่าต่ำ มูลค่าตามบัญชีสุทธิจะถูกลดลงเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="aa2be-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>





