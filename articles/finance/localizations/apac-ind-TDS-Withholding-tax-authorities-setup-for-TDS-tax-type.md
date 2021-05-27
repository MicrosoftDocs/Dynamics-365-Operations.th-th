---
title: ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายในชนิดภาษี TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าหน่วยงานจัดเก็บภาษีที่หักที่ต้นทาง (TDS)
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023620"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="87caa-103">ตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายในชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="87caa-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87caa-104">หัวข้อนี้อธิบายวิธีการตั้งค่าหน่วยงานจัดเก็บภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="87caa-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="87caa-105">ไปที่ **ภาษี \> ภาษีทางอ้อม \> หน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="87caa-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="87caa-106">[![หน้าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="87caa-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="87caa-107">ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อตั้งค่าหน่วยงานจัดเก็บภาษีหัก ณ ที่จ่ายให้กับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="87caa-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="87caa-108">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างรายการ</span><span class="sxs-lookup"><span data-stu-id="87caa-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="87caa-109">ในฟิลด์ **หน่วยงานจัดเก็บภาษีหัก ณ ที่จ่าย** ให้ป้อนชื่อสำหรับหน่วยงานจัดเก็บภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="87caa-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="87caa-110">ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="87caa-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="87caa-111">ใน FastTab **General** ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือกบัญชีผู้จัดจำหน่ายสำหรับหน่วยงานจัดเก็บภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="87caa-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87caa-112">คุณต้องกําหนดชื่อของธนาคารที่ซึ่งเงินฝากธนาคารที่เป็นหนี้ผู้จัดจำหน่ายของหน่วยงานจัดเก็บภาษี TDS จะถูกฝากไว้</span><span class="sxs-lookup"><span data-stu-id="87caa-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="87caa-113">ชื่อของธนาคารจะถูกกําหนดอยู่ในหน้า **บัญชีธนาคาร** (**บัญชีเจ้าหนี้ \> ผู้จัดจำหน่ายทั้งหมด \> ผู้จัดจำหน่าย \> การตั้งค่า \> บัญชีธนาคาร**)</span><span class="sxs-lookup"><span data-stu-id="87caa-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="87caa-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="87caa-114">Close the page.</span></span>
