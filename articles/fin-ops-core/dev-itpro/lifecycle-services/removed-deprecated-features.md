---
title: คุณลักษณะที่ถูกเอาออกหรือเลิกใช้ใน Lifecycle Services (LCS)
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจาก Microsoft Dynamics Lifecycle Services (LCS)
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b49a6f26b4c2fa895fe0e49f716ce423c3c0057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559096"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>คุณลักษณะที่ถูกเอาออกหรือเลิกใช้ใน Lifecycle Services (LCS)

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออกหรือเลิกใช้สำหรับ Microsoft Dynamics Lifecycle Services (LCS)

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในบริการอีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อให้คุณสามารถพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้เมื่อคุณทำการวางแผนของคุณเอง

## <a name="october-2019-announcements"></a>การประกาศของเดือนตุลาคม 2019

### <a name="flowchart-diagrams-in-business-process-modeler"></a>ไดอะแกรมแผนผังลำดับงานในตัวทำแบบจำลองกระบวนการทางธุรกิจ

<table>
<tbody>
<tr>
<td><strong>เหตุผลสำหรับการยกเลิกการใช้/การลบ</strong></td>
<td>เรากำลังเลิกใช้ส่วนประกอบไดอะแกรมแผนผังลำดับงานในตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM) เนื่องจากการออกแบบดั้งเดิมทำให้เกิดการใช้งานต่ำ</td>
</tr>
<tr>
<td><strong>แทนที่ ด้วยลักษณะการทำงานอื่นหรือไม่</strong></td>
<td>ไม่</td>
</tr>
<tr>
<td><strong>ส่วนที่ได้รับผล</strong></td>
<td>ตัวทำแบบจำลองกระบวนการทางธุรกิจ</td>
</tr>
<tr>
<td><strong>สถานะ</strong></td>
<td>ไม่สนับสนุน: ส่วนประกอบไดอะแกรมแผนผังลำดับงานใน BPM ถูกคาดว่าจะถูกลบออกในปี 2020 ฟังก์ชันการทำงานต่อไปนี้จะใช้งานไม่ได้:
<ul>
<li>แผนผังลำดับงานทั้งหมดจะเป็นแบบอ่านอย่างเดียวและไม่พร้อมใช้งานสำหรับการแก้ไข คุณสมบัติรูปร่างที่สัมพันธ์กับกิจกรรมแผนผังลำดับงานจะยังไม่พร้อมใช้งาน แผนผังลำดับงานเหล่านี้รวมทั้งแผนผังลำดับงานเริ่มต้นที่ถูกสร้างขึ้นโดยอัตโนมัติและแผนผังลำดับงานที่กำหนดเองที่มีการปรับเปลี่ยนตามแผนผังลำดับงานเริ่มต้นเหล่านั้น</li>
<li>ขั้นตอนของกระบวนการจะเป็นแบบอ่านอย่างเดียว และไม่พร้อมใช้งานสำหรับการแก้ไข</li>     
<li>คุณลักษณะการวิเคราะห์ความเหมาะสม/ช่องว่างแบบดั้งเดิมจะไม่พร้อมใช้งาน ดังนั้น จึงไม่มีการสร้างรายการช่องว่างโดยอัตโนมัติหรือพร้อมใช้งานสำหรับการส่งออก
<p><strong>หมายเหตุ:</strong> คุณลักษณะนี้ได้ถูกเลิกใช้งานแล้ว และถูกแทนที่ด้วยการรวม Microsoft Azure DevOps</p>
</li>
<li>ประวัติรุ่นของแผนผังลำดับงานจะไม่พร้อมใช้งาน</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]