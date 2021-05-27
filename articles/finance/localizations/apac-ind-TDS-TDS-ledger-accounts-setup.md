---
title: ตั้งค่าบัญชีแยกประเภท TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภทของคุณลักษณะภาษีที่หักที่ต้นทาง (TDS)
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023627"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="585e0-103">ตั้งค่าบัญชีแยกประเภท TDS</span><span class="sxs-lookup"><span data-stu-id="585e0-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="585e0-104">หัวข้อนี้อธิบายวิธีการตั้งค่าบัญชีแยกประเภทของคุณลักษณะภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="585e0-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="585e0-105">คุณใช้หน้า **ผังบัญชี** เพื่อตั้งค่าบัญชีแยกประเภทสำหรับ TDS</span><span class="sxs-lookup"><span data-stu-id="585e0-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="585e0-106">ไปที่ **บัญชีแยกประเภททั่วไป \> ผังบัญชี \> บัญชี \> บัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="585e0-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="585e0-107">บนแท็บ **ภาพรวม** ให้เลือก **Alt+N** เพื่อสร้างบัญชีแยกประเภท TDS และป้อนรายละเอียดที่ต้องใช้</span><span class="sxs-lookup"><span data-stu-id="585e0-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="585e0-108">บนแท็บ **การตั้งค่า** ในฟิลด์ **ชนิดของการลงรายการบัญชี** เลือก **ภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="585e0-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="585e0-109">บัญชีแยกประเภทที่มีชนิดการลงรายการบัญชีของ **ภาษีหัก ณ ที่จ่าย** สามารถกําหนดเป็นบัญชีลูกหนี้ที่ใช้ลงรายการบัญชียอดเงินลูกหนี้ TDS สำหรับรหัสภาษี TDS เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="585e0-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="585e0-110">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="585e0-110">Close the page.</span></span>
