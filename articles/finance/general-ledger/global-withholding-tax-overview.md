---
title: ภาษีหัก ณ ที่จ่ายทั่วโลก
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการหักภาษี ณ ที่จ่ายแบบสากลและวิธีการตั้งค่า ฟังก์ชันการหักภาษี ณ ที่จ่ายแบบสากลถูกปรับปรุงสำหรับธุรกรรมของผู้จัดจำหน่ายและลูกค้า เพื่อให้ภาษีหัก ณ ที่จ่ายมีการคำนวณที่ระดับสินค้า
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075749"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="4aa42-104">ภาษีหัก ณ ที่จ่ายทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="4aa42-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aa42-105">หัวข้อนี้แสดงข้อมูลเกี่ยวกับฟังก์ชันการหักภาษี ณ ที่จ่ายแบบสากลและอธิบายวิธีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="4aa42-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="4aa42-106">ฟังก์ชันใหม่มีอยู่ในรุ่น 10.0.17 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4aa42-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="4aa42-107">ฟังก์ชันการหักภาษี ณ ที่จ่ายแบบสากลถูกปรับปรุงสำหรับธุรกรรมของผู้จัดจำหน่ายและลูกค้า เพื่อให้ภาษีหัก ณ ที่จ่ายมีการคำนวณที่ระดับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4aa42-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="4aa42-108">ยอดดุลในบัญชีภาษีหัก ณ ที่จ่ายจากธุรกรรมการซื้อสามารถชำระได้โดยการใช้งานการชําระภาษีหัก ณ ที่จ่ายกับบัญชีการชําระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="4aa42-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="4aa42-109">ภาษีหัก ณ ที่จ่ายแบบสากลไม่สนับสนุนฟังก์ชัน **รักษาค่าธรรมเนียม** บนหน้าใบสั่งซื้อ ใบแจ้งหนี้ของผู้จัดจำหน่าย และใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="4aa42-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="4aa42-110">เปิดภาษีหัก ณ ที่จ่ายแบบสากล</span><span class="sxs-lookup"><span data-stu-id="4aa42-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="4aa42-111">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้เลือก **ภาษีหัก ณ ที่จ่ายแบบสากล** และจากนั้นเลือก **เปิดใช้งานเดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="4aa42-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="4aa42-112">ไปที่ **ภาษี \> การตั้งค่า \> พารามิเตอร์ \> พารามิเตอร์บัญชีแยกประเภททั่วไป** และจากนั้น บนแท็บ **ภาษีหัก ณ ที่จ่าย** ให้ตั้งค่าตัวเลือก **เปิดใช้งานภาษีหัก ณ ที่จ่ายแบบสากล** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4aa42-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="4aa42-113">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4aa42-113">Select **Save**.</span></span>
4. <span data-ttu-id="4aa42-114">รีเฟรชหน้าในเว็บเบราเซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4aa42-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4aa42-115">ฟังก์ชันภาษีหัก ณ ที่จ่ายแบบสากลไม่สามารถเปิดใช้ในประเทศ/ภูมิภาคที่มีโซลูชันภาษีหัก ณ ที่จ่ายแบบท้องถิ่นมีอยู่แล้วได้</span><span class="sxs-lookup"><span data-stu-id="4aa42-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="4aa42-116">พื้นที่เหล่านี้ประกอบด้วยแต่ไม่รวมถึงอินเดีย บราซิล ไทย ซาอุดีอาระเบีย ไอร์แลนด์ สหราชอาณาจักร และสหรัฐอเมริกา</span><span class="sxs-lookup"><span data-stu-id="4aa42-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
