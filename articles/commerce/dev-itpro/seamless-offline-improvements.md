---
title: สวิตช์ออฟไลน์ที่ไม่มีขอบเขตสำหรับบัตรของขวัญและการดำเนินงานใบลดหนี้
description: หัวข้อนี้แสดงภาพรวมของการปรับปรุงที่มีสวิตช์ออฟไลน์ที่ไม่มีขอบเขตสำหรับชนิดการชำระเงินที่เฉพาะเจาะจง
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230680"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="462fb-103">สวิตช์ออฟไลน์ที่ไม่มีขอบเขตสำหรับบัตรของขวัญและการดำเนินงานใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="462fb-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="462fb-104">ถ้าอุปกรณ์ที่ใช้ในการขายหน้าร้าน (POS) ขาดการเชื่อมต่อกับฐานข้อมูลช่องทาง การดำเนินงาน POS และธุรกรรมที่อยู่ระหว่างดำเนินการส่วนใหญ่จะสามารถดำเนินการต่อได้หลังจากที่แคชเชียร์ได้รับข้อความแจ้งเตือนเกี่ยวกับการขาดการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="462fb-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="462fb-105">อย่างไรก็ตาม ในบางกรณีธุรกรรมจะมีองค์ประกอบที่ขึ้นกับบริการแบบเรียลไทม์ และองค์ประกอบเหล่านั้นจะไม่ได้รับการสนับสนุนเมื่อ POS ทำงานแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="462fb-106">หัวข้อนี้จะอธิบายถึงฟังก์ชันบางอย่างที่ช่วยลดผลกระทบของการเชื่อมต่อที่ขาดหายไปในสถานการณ์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="462fb-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="462fb-107">การทำธุรกรรมของบัตรของขวัญให้เสร็จสมบูรณ์ในโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="462fb-108">บัตรของขวัญภายในจะขึ้นอยู่กับบริการแบบเรียลไทม์ เนื่องจากยอดดุลสำหรับบัตรของขวัญจะต้องได้รับการดูแลรักษาในศูนย์ควบคุมของ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="462fb-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="462fb-109">เพื่อช่วยป้องกันการฉ้อโกงหรือปัญหาการซิงโครไนส์อื่นๆ บัตรของขวัญจะถูกล็อคทันทีที่ถูกเพิ่มลงในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="462fb-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="462fb-110">ฟังก์ชันการล็อคจะช่วยให้มั่นใจว่าไม่สามารถใช้บัตรของขวัญบนเทอร์มินัลต่างๆ ในเวลาเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="462fb-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="462fb-111">เมื่อธุรกรรมเสร็จสมบูรณ์แล้ว บัตรของขวัญจะถูกอัปเดตและปลดล็อค</span><span class="sxs-lookup"><span data-stu-id="462fb-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="462fb-112">อย่างไรก็ตาม ถ้า POS ขาดการเชื่อมต่อหลังจากที่มีการเพิ่มบัตรของขวัญลงในธุรกรรม บัตรของขวัญอาจไม่สามารถใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="462fb-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="462fb-113">เพื่อช่วยป้องกันสถานการณ์นี้ Dynamics 365 Commerce มีพารามิเตอร์ที่เปิดใช้งานธุรกรรมที่มีบรรทัดบัตรของขวัญที่จะทำให้เสร็จสมบูรณ์ในขณะที่ POS ทำงานแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="462fb-114">เมื่อมีการเปิดใช้งานพารามิเตอร์นี้ ธุรกรรมบัตรของขวัญที่บังคับใช้แบบออฟไลน์จะถูกบันทึกพร้อมกับธุรกรรมแบบออฟไลน์ และธุรกรรมเหล่านี้จะถูกซิงค์กับศูนย์ควบคุม Commerce เมื่อมีการซิงค์ธุรกรรมแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="462fb-115">การซิงโครไนส์จะปลดล็อคบัตรของขวัญเพื่อให้สามารถใช้งานได้ที่เทอร์มินัลอื่น</span><span class="sxs-lookup"><span data-stu-id="462fb-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="462fb-116">เมื่อต้องการเปิดใช้งานฟังก์ชันเพื่อสรุปธุรกรรมบัตรของขวัญหลังจากสลับไปโหมดออฟไลน์ ให้ไปที่แท็บ **การลงรายการบัญชี** บนหน้า **พารามิเตอร์ Commerce**</span><span class="sxs-lookup"><span data-stu-id="462fb-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="462fb-117">บนแท็บนั้น ให้ค้นหาตำแหน่งแท็บด่วน **บัตรของขวัญ** และตั้งค่า **อนุญาตให้ทำธุรกรรมบัตรของขวัญที่สรุปในโหมดออฟไลน์** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="462fb-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![การตั้งค่าบัตรของขวัญแบบออฟไลน์](../media/gift.png)

<span data-ttu-id="462fb-119">โดยทั่วไปพารามิเตอร์ Commerce มีการแคช</span><span class="sxs-lookup"><span data-stu-id="462fb-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="462fb-120">หลังจากที่มีการอัปเดตการตั้งค่าของพารามิเตอร์นี้และมีการเริ่มต้นกำหนดการกระจายเพื่อซิงค์การเปลี่ยนแปลงไปยังช่องทาง การเปลี่ยนแปลงอาจใช้เวลานานถึง 24 ชั่วโมงกว่าจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="462fb-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="462fb-121">เมื่อต้องการให้การเปลี่ยนแปลงมีผลบังคับใช้ทันที ให้รีเซ็ต Microsoft Internet Information Services (IIS) ใหม่</span><span class="sxs-lookup"><span data-stu-id="462fb-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="462fb-122">การทำธุรกรรมของใบลดหนี้ให้เสร็จสมบูรณ์ในโหมดออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="462fb-123">เช่นเดียวกับบัตรของขวัญภายใน ใบลดหนี้จะถูกเก็บรักษาไว้ที่ศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="462fb-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="462fb-124">Commerce มีพารามิเตอร์ที่เปิดใช้งานธุรกรรมใบลดหนี้ให้เสร็จสมบูรณ์ในขณะที่ POS ทำงานแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="462fb-125">พารามิเตอร์นี้ทำงานเหมือนกับพารามิเตอร์บัตรของขวัญที่กล่าวถึงในหัวข้อก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="462fb-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="462fb-126">เมื่อมีการเปิดใช้งานพารามิเตอร์ ธุรกรรมใบลดหนี้ที่บังคับใช้แบบออฟไลน์จะถูกซิงค์กลับไปยังฐานข้อมูลช่องทาง พร้อมกับธุรกรรมอื่นๆ ที่ดำเนินการในขณะที่ POS ทำงานแบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="462fb-127">เมื่อต้องการเปิดใช้งานฟังก์ชันเพื่อสรุปธุรกรรมใบลดหนี้หลังจากสลับไปโหมดออฟไลน์ ให้ไปที่แท็บ **การลงรายการบัญชี** บนหน้า **พารามิเตอร์ Commerce**</span><span class="sxs-lookup"><span data-stu-id="462fb-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="462fb-128">บนแท็บนั้น ให้ค้นหาตำแหน่งแท็บด่วน **ใบลดหนี้** และตั้งค่า **อนุญาตให้ทำธุรกรรมใบลดหนี้ที่สรุปในโหมดออฟไลน์** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="462fb-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![การตั้งค่าใบลดหนี้ออฟไลน์](../media/creditmemo.png)

<span data-ttu-id="462fb-130">โดยทั่วไปพารามิเตอร์ Commerce มีการแคช</span><span class="sxs-lookup"><span data-stu-id="462fb-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="462fb-131">หลังจากที่มีการอัปเดตการตั้งค่าของพารามิเตอร์นี้และมีการเริ่มต้นกำหนดการกระจายเพื่อซิงค์การเปลี่ยนแปลงไปยังช่องทาง การเปลี่ยนแปลงอาจใช้เวลานานถึง 24 ชั่วโมงกว่าจะมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="462fb-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="462fb-132">ถ้าต้องการให้การเปลี่ยนแปลงมีผลบังคับใช้ทันที ให้รีเซ็ต IIS</span><span class="sxs-lookup"><span data-stu-id="462fb-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="462fb-133">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="462fb-133">Related topics</span></span>

- [<span data-ttu-id="462fb-134">ฟังก์ชันการขายหน้าร้าน (POS) แบบออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="462fb-135">การดำเนินงานการขายหน้าร้าน (POS) แบบออนไลน์และออฟไลน์</span><span class="sxs-lookup"><span data-stu-id="462fb-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]