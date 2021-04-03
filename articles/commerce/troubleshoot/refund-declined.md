---
title: การขอคืนเงินของใบสั่งส่งคืนสินค้าได้รับการปฏิเสธ
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการปฏิเสธการขอคืนเงินในใบสั่งส่งคืนสินค้า เนื่องจากบัตรเครดิตที่ใช้สําหรับการออกใบแจ้งหนี้แตกต่างจากบัตรที่ใช้ในระหว่างการตรวจสอบการออกใบแจ้งหนี้ดั้งเดิม
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
ms.openlocfilehash: e202c6b4b9e025d5af1cd5eb6235884aab6444e6
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585561"
---
# <a name="refund-on-a-return-order-is-declined"></a><span data-ttu-id="a02ad-103">การขอคืนเงินของใบสั่งส่งคืนสินค้าได้รับการปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="a02ad-103">Refund on a return order is declined</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a02ad-104">หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อมีการปฏิเสธการขอคืนเงินในใบสั่งส่งคืนสินค้า เนื่องจากบัตรเครดิตที่ใช้สําหรับการออกใบแจ้งหนี้แตกต่างจากบัตรที่ใช้ในระหว่างการตรวจสอบการออกใบแจ้งหนี้ดั้งเดิม</span><span class="sxs-lookup"><span data-stu-id="a02ad-104">This topic provides troubleshooting guidance that can help when a refund on a return order is declined because the credit card that is used for invoicing differs from the card that was used during the original payment authorization.</span></span>

## <a name="description"></a><span data-ttu-id="a02ad-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="a02ad-105">Description</span></span>

<span data-ttu-id="a02ad-106">การขอคืนเงินได้รับการปฏิเสธเมื่อบัตรเครดิตที่ใช้ในการออกใบแจ้งหนี้ใบสั่งส่งคืนสินค้าแตกต่างจากบัตรที่ใช้ในระหว่างการอนุมัติการชำระเงินครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="a02ad-106">A refund is declined when the credit card that is used to invoice a return order differs from the card that was used during the original payment authorization.</span></span> <span data-ttu-id="a02ad-107">คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "การชำระเงินบางรายการไม่อยู่ในสถานะที่ถูกต้องในการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="a02ad-107">You receive the following error message: "Some payments are not in the correct status for posting.</span></span> <span data-ttu-id="a02ad-108">โปรดตรวจสอบความถูกต้องของสถานะการชำระเงินทั้งหมดอีกครั้งก่อนการออกใบแจ้งหนี้"</span><span class="sxs-lookup"><span data-stu-id="a02ad-108">Please re-validate the status of all payments prior to invoicing."</span></span>

<span data-ttu-id="a02ad-109">รายละเอียดการตรวจสอบการชำระเงินจะรวมข้อความแสดงข้อผิดพลาดต่อไปนี้: "เกตเวย์ Adyen SendRequest() ล้มเหลวโดยมีสถานะ 'InternalServerError'.22144; การตอบสนองว่างเปล่าที่ส่งคืนจาก Adyen (22001);"</span><span class="sxs-lookup"><span data-stu-id="a02ad-109">The payment authorization details will include the following error message: "Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);"</span></span>

![ปฏิเสธการขอคืนเงินจากข้อผิดพลาดของใบสั่งส่งคืนสินค้า](media/refund-order-decline.jpg)

## <a name="resolution"></a><span data-ttu-id="a02ad-111">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="a02ad-111">Resolution</span></span>

### <a name="enable-blind-returns-in-adyen"></a><span data-ttu-id="a02ad-112">เปิดใช้งานการส่งคืนที่ซ่อนใน Adyen</span><span class="sxs-lookup"><span data-stu-id="a02ad-112">Enable blind returns in Adyen</span></span>

<span data-ttu-id="a02ad-113">หากต้องการเปิดใช้งานการส่งคืนที่ซ่อนอยู่ ให้ปฏิบัติตามขั้นตอนใน [การแก้ไขปัญหาข้อผิดพลาดเกี่ยวกับ Dynamics 365 Payment Connector ของปัญหา Adyen](adyen-support.md) เพื่อติดต่อทีมสนับสนุน Adyen และขอให้เปิดใช้งานการส่งคืนที่ซ่อนอยู่บนบัญชีร้านค้า Adyen ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a02ad-113">To enable blind returns, follow the steps in [Troubleshoot Dynamics 365 Payment Connector for Adyen issues](adyen-support.md) to contact the Adyen support team and request that blind returns be enabled on your Adyen merchant account.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a02ad-114">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a02ad-114">Additional resources</span></span>

[<span data-ttu-id="a02ad-115">ตัวเชื่อมต่อการชำระเงิน Dynamics 365 สำหรับ Adyen</span><span class="sxs-lookup"><span data-stu-id="a02ad-115">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="a02ad-116">ตั้งค่าตัวเชื่อมต่อการชำระเงิน Adyen สำหรับ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a02ad-116">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
