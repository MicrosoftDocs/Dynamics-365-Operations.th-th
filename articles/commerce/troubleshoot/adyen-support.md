---
title: ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen
description: หัวข้อนี้มีคำแนะนำในการแก้ไขปัญหาซึ่งสามารถให้ความช่วยเหลือคุณเมื่อคุณมีปัญหาเกี่ยวกับ Microsoft Dynamics 365 Payment Connector สําหรับ Adyen
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
ms.openlocfilehash: 707efeba9553b996e4e33a4754e42a9d22643e33
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019600"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="f8cde-103">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="f8cde-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8cde-104">หัวข้อนี้มีคำแนะนำในการแก้ไขปัญหาซึ่งสามารถให้ความช่วยเหลือคุณเมื่อคุณมีปัญหาเกี่ยวกับ Microsoft Dynamics 365 Payment Connector สําหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="f8cde-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="f8cde-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f8cde-105">Description</span></span>

<span data-ttu-id="f8cde-106">คุณมีปัญหาเกี่ยวกับ Dynamics 365 Payment Connector สำหรับ Adyen ในพื้นที่ต่อไปนี้และคุณต้องการความช่วยเหลือจากทีมงาน Adyen</span><span class="sxs-lookup"><span data-stu-id="f8cde-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="f8cde-107">การตั้งค่าคอนฟิกของการขายหน้าร้าน (POS) การขายหน้าร้านแบบสมัยใหม่ (MPOS) ศูนย์บริการ หรือ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8cde-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="f8cde-108">หมายเลขอ้างอิงของ Adyen Payment Service (PSP) (ตัวอย่างเช่น ถ้าคุณมีคำถามเกี่ยวกับการปฏิเสธ รวมถึงการปฏิเสธการคีย์ด้วยตนเอง \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="f8cde-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="f8cde-109">สิ่งที่ไม่ได้อยู่ในสภาพแวดล้อมการทดสอบหรือสภาพแวดล้อมของผู้ขายที่ใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="f8cde-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="f8cde-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="f8cde-110">Resolution</span></span>

<span data-ttu-id="f8cde-111">ใช้เท็มเพลตอีเมลต่อไปนี้เพื่อเริ่มกระบวนการให้ความช่วยเหลือกับทีม Adyen</span><span class="sxs-lookup"><span data-stu-id="f8cde-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="f8cde-112">เพื่อเร่งการแก้ไขปัญหาเบื้องต้น ให้ตรวจสอบให้แน่ใจว่าอีเมลมีรายละเอียดที่ต้องใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="f8cde-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="f8cde-113">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f8cde-113">Field</span></span>        | <span data-ttu-id="f8cde-114">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="f8cde-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="f8cde-115">ไปยัง</span><span class="sxs-lookup"><span data-stu-id="f8cde-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="f8cde-116">Cc</span><span class="sxs-lookup"><span data-stu-id="f8cde-116">Cc</span></span>           | |
| <span data-ttu-id="f8cde-117">บรรทัดหัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="f8cde-117">Subject line</span></span> | <span data-ttu-id="f8cde-118">คำขอการสนับสนุน Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="f8cde-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="f8cde-119">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="f8cde-119">Body</span></span>         | <p><span data-ttu-id="f8cde-120">สวัสดี ฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="f8cde-120">Hi Support,</span></span></p><p><span data-ttu-id="f8cde-121">กรุณาให้ความช่วยเหลือเกี่ยวกับปัญหาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f8cde-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="f8cde-122">บัญชีผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="f8cde-122">Merchant account</span></span></li><li><span data-ttu-id="f8cde-123">สภาพแวดล้อม (การทดสอบ/การผลิต)</span><span class="sxs-lookup"><span data-stu-id="f8cde-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="f8cde-124">ช่องทาง (POS/ศูนย์บริการ/Commerce e-commerce)</span><span class="sxs-lookup"><span data-stu-id="f8cde-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="f8cde-125">หมายเลขอ้างอิง PSP ถ้าปัญหามีความเกี่ยวข้องกับธุรกรรมหนึ่งๆ (คุณสามารถค้นหาหมายเลขอ้างอิง PSP บนใบเสร็จ ใน Adyen Customer Area หรือในเมนูธุรกรรมบนเทอร์มินัล POS)</span><span class="sxs-lookup"><span data-stu-id="f8cde-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="f8cde-126">ภาพหน้าจอหรือรูปภาพของข้อความแสดงข้อผิดพลาด ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="f8cde-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="f8cde-127">บันทึกตัวแสดงเหตุการณ์ (ในรูปแบบ .txt)</span><span class="sxs-lookup"><span data-stu-id="f8cde-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="f8cde-128">อธิบายปัญหาและขั้นตอนการแก้ไขปัญหาที่คุณพยายามแล้ว</span><span class="sxs-lookup"><span data-stu-id="f8cde-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="f8cde-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f8cde-129">Additional resources</span></span>

[<span data-ttu-id="f8cde-130">ยอมรับการชำระเงินโดยตัวเชื่อมต่อ Adyen สำหรับ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f8cde-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="f8cde-131">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="f8cde-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="f8cde-132">ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f8cde-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
