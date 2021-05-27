---
title: การรวมเงินคืนของลูกค้าล้มเหลว เมื่อมีการใช้กลุ่มเงินคืนของสินค้า
description: เมื่อคุณใช้ข้อตกลงเงินคืนของลูกค้าโดยรวมกับกลุ่มเงินคืนของสินค้า เงินคืนจะถูกคํานวณ แต่การรวบรวมจะล้มเหลว
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026939"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="23316-103">การรวมเงินคืนของลูกค้าล้มเหลว เมื่อมีการใช้กลุ่มเงินคืนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="23316-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="23316-104">หมายเลข KB: 4611372</span><span class="sxs-lookup"><span data-stu-id="23316-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="23316-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="23316-105">Symptoms</span></span>

<span data-ttu-id="23316-106">เมื่อคุณใช้ข้อตกลงเงินคืนของลูกค้า (ของชนิด *จำนวน*) โดยรวมกับกลุ่มเงินคืนของสินค้า เงินคืนจะถูกคํานวณ แต่การรวบรวมจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="23316-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="23316-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="23316-107">Resolution</span></span>

<span data-ttu-id="23316-108">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="23316-108">The system is behaving as designed.</span></span> <span data-ttu-id="23316-109">กลุ่มสินค้าจะจัดกลุ่มเฉพาะสินค้าที่มีเงื่อนไขขีดจำกัดเดียวกันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="23316-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="23316-110">เงื่อนไขเงินคืน (ขีดจำกัด) ถูกตั้งค่าโดยเทียบกับยอดเงินสำหรับสินค้าแต่ละรายการ ไม่ใช่เทียบกับยอดเงินสะสมสำหรับสินค้าใดๆ ในกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="23316-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
