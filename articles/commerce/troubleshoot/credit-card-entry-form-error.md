---
title: หน้ารายการบัตรเครดิตแสดงข้อผิดพลาดขณะชำระเงิน
description: หัวข้อนี้ให้แนวทางแก้ไขปัญหาที่สามารถช่วยได้เมื่อไม่ได้โหลดส่วนวิธีการชำระเงินและแสดงข้อความแสดงข้อผิดพลาด
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ea9105481e6c5812565f0d3604906c905bcb5443
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018517"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="6f987-103">หน้ารายการบัตรเครดิตแสดงข้อผิดพลาดขณะชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6f987-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f987-104">หัวข้อนี้ให้แนวทางแก้ไขปัญหาที่สามารถช่วยได้เมื่อไม่ได้โหลดส่วน **วิธีการชำระเงิน** และแสดงข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="6f987-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="6f987-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6f987-105">Description</span></span>

<span data-ttu-id="6f987-106">เมื่อคุณเปิดหน้าชำระเงินของร้านค้าออนไลน์ส่วน  **วิธีการชำระเงิน** จะไม่ถูกโหลด และข้อความแสดงข้อผิดพลาดต่อไปนี้จะปรากฎขึ้น "มีบางอย่างผิดปกติ</span><span class="sxs-lookup"><span data-stu-id="6f987-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="6f987-107">กรุณาลองใหม่อีกครั้งในภายหลัง"</span><span class="sxs-lookup"><span data-stu-id="6f987-107">Please try again later."</span></span>

![ข้อผิดพลาดของโมดูลการชำระเงิน](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="6f987-109">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="6f987-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="6f987-110">รอให้แคช Commerce Scale Unit หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="6f987-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="6f987-111">การตั้งค่าบริการชำระเงินในหน้าชำระเงินของร้านค้าออนไลน์จะถูกแคชบน Commerce Scale Unit และอาจใช้เวลาถึง 15 นาทีจึงจะปรากฏบนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="6f987-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="6f987-112">การตั้งค่าบริการชำระเงินเหล่านี้รวมถึงการเปลี่ยนแปลงรหัสบัญชีผู้ขาย คีย์ Cloud API และการตั้งค่าการกำหนดค่าคอนฟิกต่างๆ ที่เกี่ยวข้องกับวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6f987-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f987-113">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6f987-113">Additional resources</span></span>

[<span data-ttu-id="6f987-114">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="6f987-114">Set up an online channel</span></span>](../channel-setup-online.md)
