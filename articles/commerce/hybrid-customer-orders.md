---
title: ใบสั่งของลูกค้าแบบไฮบริด
description: ใบสั่งของลูกค้าไฮบริดเป็นใบสั่งเดียว ซึ่งประกอบด้วยผลิตภัณฑ์ที่ลูกค้าสามารถดำเนินการจากร้านได้ รวมถึงผลิตภัณฑ์ที่จะถูกเบิกสินค้าหรือจัดส่งได้ในภายหลัง
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6357c034059523f83ba05a1da53cae691ef74758
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798948"
---
# <a name="hybrid-customer-orders"></a><span data-ttu-id="27309-103">ใบสั่งของลูกค้าแบบไฮบริด</span><span class="sxs-lookup"><span data-stu-id="27309-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27309-104">ใบสั่งของลูกค้าไฮบริดเป็นใบสั่งเดียว ซึ่งประกอบด้วยผลิตภัณฑ์ที่ลูกค้าสามารถดำเนินการจากร้านได้ รวมถึงผลิตภัณฑ์ที่จะถูกเบิกสินค้าหรือจัดส่งได้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="27309-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="27309-105">ในการค้าคุณสามารถเลือกดำเนินการผลิตภัณฑ์ทั้งหมดหรือดำเนินการผลิตภัณฑ์ที่เลือกสำหรับใบสั่งของลูกค้าอย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="27309-105">In Commerce, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="27309-106">บรรทัดผลิตภัณฑ์ที่มีการทำเครื่องหมายไว้เป็น ดำเนินการ จะถูกออกใบแจ้งหนี้โดยอัตโนมัติหลังจากที่มีการสร้างใบสั่ง ในทำนองเดียวกันนี้จะเหมือนกันสำหรับใบสั่งที่จะถูกเบิกสินค้าหลังจากที่มีการสร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="27309-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="27309-107">ยอดเงินที่ครบกำหนดในใบสั่งไฮบริดจะถูกกำหนดโดยการเพิ่มเปอร์เซ็นต์เงินฝากในบรรทัดการเบิกและการจัดส่งสินค้าที่มียอดเงินเต็มของบรรทัดดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="27309-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="27309-108">สำหรับใบสั่งไฮบริด ระบบจะสลับไปมาระหว่างโหมดใบสั่งของลูกค้าและโหมดเงินสดและดำเนินการดังนี้:</span><span class="sxs-lookup"><span data-stu-id="27309-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

- <span data-ttu-id="27309-109">ถ้าผลิตภัณฑ์ทั้งหมดในรถเข็นถูกตั้งค่าเป็น **ดำเนินการจัดส่ง** ใบสั่งจะถูกจัดการโดยถือเป็นธุรกรรมเงินสดและดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="27309-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
- <span data-ttu-id="27309-110">ถ้าบรรทัดใดๆ หรือทุกบรรทัดในรถเข็นถูกตั้งค่าเป็น **รับ** หรือ **จัดส่งการจัดส่ง** ใบสั่งจะถูกจัดการโดยถือเป็นธุรกรรมใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="27309-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="27309-111">ถ้าบรรทัดรถเข็นถูกเลือก และมีการเลือก **เบิกสินค้าที่เลือก** **จัดส่งที่เลือก** หรือ **ดำเนินการกับรายการที่เลือก** เฉพาะบรรทัดรถเข็นจะถูกตั้งค่าด้วยวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="27309-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="27309-112">ในกรณีดังกล่าว ขั้นตอนปลายน้ำของการดำเนินงานเป็นต่อไปตามปกติ</span><span class="sxs-lookup"><span data-stu-id="27309-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="27309-113">อย่างไรก็ตาม ถ้า **เบิกสินค้าที่เลือก** **จัดส่งที่เลือก** หรือ **ดำเนินการกับรายการที่เลือก** โดยไม่มีการเลือกบรรทัดรถเข็นไว้ ระบบจะเปิดหน้าใหม่ที่แสดงรายการทั้งหมดในรายการในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="27309-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="27309-114">บนหน้าจอนั้น คุณสามารถเลือกหลายบรรทัดพร้อมกันสำหรับการตั้งค่าวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="27309-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="27309-115">เมื่อคุณใช้วิธีนั้นสำหรับการเลือกบรรทัด วิธีการจัดส่งใด ๆ ก่อนหน้านี้ที่ได้ถูกกำหนดให้กับบรรทัดจะถูกแทน</span><span class="sxs-lookup"><span data-stu-id="27309-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27309-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="27309-116">Additional resources</span></span>

[<span data-ttu-id="27309-117">ใบสั่งของลูกค้าใน Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="27309-117">Customer orders in Modern POS (MPOS)</span></span>](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]