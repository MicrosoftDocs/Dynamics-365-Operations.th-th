---
title: โมดูลไอคอนรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793092"
---
# <a name="cart-icon-module"></a><span data-ttu-id="d307d-103">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="d307d-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d307d-104">หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d307d-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d307d-105">โมดูลไอคอนรถเข็นแสดงถึงรถเข็นในส่วนหัวของหน้าและแสดงจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="d307d-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="d307d-106">โมดูลไอคอนรถเข็นยังแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="d307d-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="d307d-107">รถเข็นแบบมินิให้ผู้ใช้ได้รับสรุปของสินค้าในรถเข็นโดยไม่ต้องนำทางไปยังหน้ารถเข็น</span><span class="sxs-lookup"><span data-stu-id="d307d-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="d307d-108">นอกจากนี้ยังช่วยให้ผู้ใช้สามารถไปยังหน้าการเช็คเอาท์โดยตรงหากพอใจกับสรุป</span><span class="sxs-lookup"><span data-stu-id="d307d-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="d307d-109">การทำเช่นนี้จะช่วยลดจำนวนการนำทางของหน้าและทำการเช็คเอาท์ได้รวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="d307d-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="d307d-110">การสนับสนุนสำหรับโมดูลไอคอนรถเข็นมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.11</span><span class="sxs-lookup"><span data-stu-id="d307d-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="d307d-111">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลไอคอนรถเข็นที่แสดงรถเข็นมินิในส่วนหัวของ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="d307d-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![ตัวอย่างของโมดูลไอคอนรถเข็น](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="d307d-113">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="d307d-113">Module properties</span></span>

- <span data-ttu-id="d307d-114">**แสดงรถเข็นแบบมินิ** – เมื่อเป็นจริง คุณสมบัตินี้จะเปิดใช้งานสรุปรถเข็น (รถเข็นมินิ) ที่จะแสดงเมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="d307d-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="d307d-115">ฟังก์ชันนี้ได้รับการสนับสนุนสำหรับพอร์ตมุมมองเดสก์ท็อปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="d307d-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="d307d-116">เพิ่มโมดูลไอคอนรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="d307d-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="d307d-117">เมื่อต้องการเพิ่มโมดูลไอคอนรถเข็น ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="d307d-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d307d-118">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d307d-118">Additional resources</span></span>

[<span data-ttu-id="d307d-119">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="d307d-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d307d-120">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="d307d-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d307d-121">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="d307d-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d307d-122">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d307d-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d307d-123">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d307d-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d307d-124">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="d307d-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d307d-125">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d307d-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d307d-126">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="d307d-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]