---
title: ตั้งค่าพารามิเตอร์ TDS ในบัญชีเจ้าหนี้และบัญชีลูกหนี้
description: หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ในบัญชีเจ้าหนี้และบัญชีลูกหนี้ เพื่อสนับสนุนการหักภาษีที่หักที่ต้นทาง (TDS)
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023628"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="a3257-103">ตั้งค่าพารามิเตอร์ TDS ในบัญชีเจ้าหนี้และบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="a3257-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3257-104">หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ในบัญชีเจ้าหนี้และบัญชีลูกหนี้ เพื่อสนับสนุนการหักภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="a3257-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="a3257-105">ไปที่ **ภาษี \> การตั้งค่า \> พารามิเตอร์ \> พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="a3257-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="a3257-106">บนแท็บ **อัพเดต** ให้เลือก **อัพเดตบรรทัดใบสั่ง** เพื่อเปิดกล่องโต้ตอบ **อัพเดตบรรทัดใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="a3257-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="a3257-107">ในส่วน **กลุ่ม TDS** ในฟิลด์ **การอัพเดตกลุ่ม TDS** ให้ระบุวิธีการที่จะใช้ในการอัพเดตกลุ่ม TDS ในระดับบรรทัด</span><span class="sxs-lookup"><span data-stu-id="a3257-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="a3257-108">การตั้งค่านี้จะถูกใช้เมื่อมีการอัพเดตกลุ่ม TDS บนส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a3257-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="a3257-109">โดยตัวเลือกที่คุณสามารถเลือกได้มีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a3257-109">The following options are available:</span></span>

    - <span data-ttu-id="a3257-110">**ไม่เคย** – กลุ่ม TDS จะไม่มีการอัพเดตในบรรทัดใบสั่ง เมื่อมีการอัพเดตบนส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a3257-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="a3257-111">**เสมอ** – กลุ่ม TDS จะถูกอัพเดตในบรรทัดใบสั่งโดยอัตโนมัติ เมื่อมีการอัพเดตบนส่วนหัวของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a3257-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="a3257-112">**พร้อมต์** – ผู้ใช้ได้รับข้อความที่แจ้งให้อัพเดตกลุ่ม TDS ในบรรทัดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="a3257-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="a3257-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a3257-113">Select **OK**.</span></span>

    <span data-ttu-id="a3257-114">[![กล่องโต้ตอบการอัพเดตบรรทัดใบสั่ง](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="a3257-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="a3257-115">ไปที่ **ภาษี \> การตั้งค่า \> พารามิเตอร์ \> พารามิเตอร์บัญชีเจ้าหนี้**</span><span class="sxs-lookup"><span data-stu-id="a3257-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="a3257-116">บนแท็บ **ทั่วไป** บน FastTab **แบ่งตามข้อมูลการจัดส่ง** ให้ตั้งค่าตัวเลือก **ใบรับสินค้า** เป็น **ใช่** เพื่อลงรายการบัญชีและแบ่งใบรับสินค้าที่มีที่อยู่ที่จัดส่งและหมายเลขบัญชีภาษีที่แตกต่างกัน (TANs)</span><span class="sxs-lookup"><span data-stu-id="a3257-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="a3257-117">ถ้าตั้งค่าตัวเลือกนี้เป็น **ไม่** คุณไม่สามารถลงรายการบัญชีบันทึกการจัดส่งในการซื้อที่มีที่อยู่ที่จัดส่งและ TAN ที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="a3257-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="a3257-118">ตั้งค่าตัวเลือก **ใบแจ้งหนี้** เป็น **ใช่** เพื่อลงรายการบัญชีและแบ่งใบแจ้งหนี้การซื้อที่มีที่อยู่ที่จัดส่งและ TAN ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="a3257-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="a3257-119">[![FastTab แบ่งตามข้อมูลการจัดส่ง](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="a3257-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="a3257-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a3257-120">Close the page.</span></span>
