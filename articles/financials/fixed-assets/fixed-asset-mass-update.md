---
title: การอัพเดตสินทรัพย์ถาวรโดยรวม
description: ถ้าคุณใช้สมุดบัญชี คุณสามารถเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มของสินทรัพย์ที่เป็นส่วนหนึ่งของสมุดบัญชีเดียวกัน
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b740f1fe710c2278bd5ac5f8d615f0e305cd7df1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565380"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="e4477-103">การอัพเดตสินทรัพย์ถาวรโดยรวม</span><span class="sxs-lookup"><span data-stu-id="e4477-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4477-104">ถ้าคุณใช้สมุดบัญชี คุณสามารถเปลี่ยนแบบแผนการคิดค่าเสื่อมราคาสำหรับกลุ่มของสินทรัพย์ที่เป็นส่วนหนึ่งของสมุดบัญชีเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="e4477-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="e4477-105">ตัวอย่างเช่น ถ้าคุณอยู่ในสหรัฐอเมริกา และคุณใช้สินทรัพย์ของคุณมากกว่า 40 เปอร์เซ็นต์ในบริการในระหว่างไตรมาสสี่ของปี คุณต้องใช้แบบแผนการคิดค่าเสื่อมราคากลางไตรมาส</span><span class="sxs-lookup"><span data-stu-id="e4477-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="e4477-106">คุณสามารถใช้กระบวนการสำหรับการอัพเดตโดยรวมเพื่อเปลี่ยนสินทรัพย์ทั้งหมดที่ต้องใช้แบบแผนการคิดค่าเสื่อมราคาใหม่</span><span class="sxs-lookup"><span data-stu-id="e4477-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="e4477-107">เมื่อคุณอัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ คุณลบธุรกรรมค่าเสื่อมราคาทั้งหมดที่มีอยู่สำหรับสินทรัพย์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="e4477-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="e4477-108">คุณยังจะลบธุรกรรมทั้งหมดสำหรับการปรับปรุงค่าเสื่อมราคา ธุรกรรมค่าเสื่อมราคาโบนัส และธุรกรรมค่าเสื่อมราคาพิเศษของสินทรัพย์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e4477-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="e4477-109">ถ้าต้องการอัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ซึ่งตัดจำหน่ายแล้ว คุณต้องลบธุรกรรมการตัดจำหน่ายที่มีอยู่ออกก่อน</span><span class="sxs-lookup"><span data-stu-id="e4477-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="e4477-110">คุณต้องลบธุรกรรมทั้งหมดที่สร้างขึ้นเนื่องจากกระบวนการตัดจำหน่ายออกด้วย</span><span class="sxs-lookup"><span data-stu-id="e4477-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="e4477-111">หลังจากคุณอัพเดตแบบแผนการคิดค่าเสื่อมราคาสำหรับสินทรัพย์ คุณสามารถดำเนินการในส่วนของค่าเสื่อมราคาและค่าเสื่อมราคาพิเศษของสินทรัพย์แต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="e4477-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="e4477-112">คุณยังสามารถทำการปรับปรุงค่าเสื่อมราคาด้วยตนเอง ถ้าจำเป็นต้องมีการปรับปรุงใด ๆ</span><span class="sxs-lookup"><span data-stu-id="e4477-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>





