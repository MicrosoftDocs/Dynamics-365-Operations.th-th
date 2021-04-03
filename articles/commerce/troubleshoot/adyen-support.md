---
title: ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen
description: หัวข้อนี้มีคำแนะนำในการแก้ไขปัญหาซึ่งสามารถให้ความช่วยเหลือคุณเมื่อคุณมีปัญหาเกี่ยวกับ Microsoft Dynamics 365 Payment Connector สําหรับ Adyen
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585548"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="c51f0-103">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="c51f0-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c51f0-104">หัวข้อนี้มีคำแนะนำในการแก้ไขปัญหาซึ่งสามารถให้ความช่วยเหลือคุณเมื่อคุณมีปัญหาเกี่ยวกับ Microsoft Dynamics 365 Payment Connector สําหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="c51f0-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="c51f0-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c51f0-105">Description</span></span>

<span data-ttu-id="c51f0-106">คุณมีปัญหาเกี่ยวกับ Dynamics 365 Payment Connector สำหรับ Adyen ในพื้นที่ต่อไปนี้และคุณต้องการความช่วยเหลือจากทีมงาน Adyen</span><span class="sxs-lookup"><span data-stu-id="c51f0-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="c51f0-107">การตั้งค่าคอนฟิกของการขายหน้าร้าน (POS) การขายหน้าร้านแบบสมัยใหม่ (MPOS) ศูนย์บริการ หรือ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c51f0-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="c51f0-108">หมายเลขอ้างอิงของ Adyen Payment Service (PSP) (ตัวอย่างเช่น ถ้าคุณมีคำถามเกี่ยวกับการปฏิเสธ รวมถึงการปฏิเสธการคีย์ด้วยตนเอง \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="c51f0-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="c51f0-109">สิ่งที่ไม่ได้อยู่ในสภาพแวดล้อมการทดสอบหรือสภาพแวดล้อมของผู้ขายที่ใช้งานจริง</span><span class="sxs-lookup"><span data-stu-id="c51f0-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="c51f0-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="c51f0-110">Resolution</span></span>

<span data-ttu-id="c51f0-111">ใช้เท็มเพลตอีเมลต่อไปนี้เพื่อเริ่มกระบวนการให้ความช่วยเหลือกับทีม Adyen</span><span class="sxs-lookup"><span data-stu-id="c51f0-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="c51f0-112">เพื่อเร่งการแก้ไขปัญหาเบื้องต้น ให้ตรวจสอบให้แน่ใจว่าอีเมลมีรายละเอียดที่ต้องใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c51f0-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="c51f0-113">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="c51f0-113">Field</span></span>        | <span data-ttu-id="c51f0-114">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="c51f0-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="c51f0-115">ไปยัง</span><span class="sxs-lookup"><span data-stu-id="c51f0-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="c51f0-116">Cc</span><span class="sxs-lookup"><span data-stu-id="c51f0-116">Cc</span></span>           | |
| <span data-ttu-id="c51f0-117">บรรทัดหัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="c51f0-117">Subject line</span></span> | <span data-ttu-id="c51f0-118">คำขอการสนับสนุน Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="c51f0-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="c51f0-119">เนื้อหา</span><span class="sxs-lookup"><span data-stu-id="c51f0-119">Body</span></span>         | <p><span data-ttu-id="c51f0-120">สวัสดี ฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="c51f0-120">Hi Support,</span></span></p><p><span data-ttu-id="c51f0-121">กรุณาให้ความช่วยเหลือเกี่ยวกับปัญหาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c51f0-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="c51f0-122">บัญชีผู้ขาย</span><span class="sxs-lookup"><span data-stu-id="c51f0-122">Merchant account</span></span></li><li><span data-ttu-id="c51f0-123">สภาพแวดล้อม (การทดสอบ/การผลิต)</span><span class="sxs-lookup"><span data-stu-id="c51f0-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="c51f0-124">ช่องทาง (POS/ศูนย์บริการ/Commerce e-commerce)</span><span class="sxs-lookup"><span data-stu-id="c51f0-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="c51f0-125">หมายเลขอ้างอิง PSP ถ้าปัญหามีความเกี่ยวข้องกับธุรกรรมหนึ่งๆ (คุณสามารถค้นหาหมายเลขอ้างอิง PSP บนใบเสร็จ ใน Adyen Customer Area หรือในเมนูธุรกรรมบนเทอร์มินัล POS)</span><span class="sxs-lookup"><span data-stu-id="c51f0-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="c51f0-126">ภาพหน้าจอหรือรูปภาพของข้อความแสดงข้อผิดพลาด ถ้ามี</span><span class="sxs-lookup"><span data-stu-id="c51f0-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="c51f0-127">บันทึกตัวแสดงเหตุการณ์ (ในรูปแบบ .txt)</span><span class="sxs-lookup"><span data-stu-id="c51f0-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="c51f0-128">อธิบายปัญหาและขั้นตอนการแก้ไขปัญหาที่คุณพยายามแล้ว</span><span class="sxs-lookup"><span data-stu-id="c51f0-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="c51f0-129">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c51f0-129">Additional resources</span></span>

[<span data-ttu-id="c51f0-130">ยอมรับการชำระเงินโดยตัวเชื่อมต่อ Adyen สำหรับ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c51f0-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="c51f0-131">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="c51f0-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="c51f0-132">ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="c51f0-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
