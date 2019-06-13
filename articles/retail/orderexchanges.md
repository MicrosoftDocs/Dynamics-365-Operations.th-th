<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="orderexchanges.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>orderexchanges.ba78aa.43571099727830e81c41416b6fe250dba398b3f8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>43571099727830e81c41416b6fe250dba398b3f8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\orderexchanges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่าคอนฟิกและดำเนินการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to configure an exchange on a return in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หัวข้อนี้อธิบายวิธีตั้งค่าคอนฟิกการแลกเปลี่ยนเมื่อมีการส่งคืนสินค้าใน Microsoft Dynamics 365 for Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure and process an exchange on a return order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่าคอนฟิกและดำเนินการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ใน Microsoft Dynamics 365 for Retail รุ่นก่อนหน้านี้ การส่งคืนสินค้าตามใบสั่งของลูกค้าจะได้รับการดำเนินการโดยใช้เอกสารใบสั่งส่งคืนสินค้าใน Retail Headquarters</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, the return order document can be used to process only products that are being returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ดี เราสามารถใช้เอกสารใบสั่งส่งคืนสินค้าเพื่อประมวลผลเฉพาะผลิตภัณฑ์ที่จะส่งคืนได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The returned products are indicated by a negative quantity on the return order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์ที่ส่งคืนจะบ่งชี้โดยปริมาณติดลบในรายการใบสั่งส่งคืนสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>By contrast, sales are indicated by a positive quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในทางกลับกัน การขายจะบ่งชี้โดยปริมาณที่เป็นบวก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>However, the return order document doesn't support positive quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ดี เอกสารใบสั่งส่งคืนสินค้าจะไม่สนับสนุนปริมาณที่เป็นบวก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ด้วยข้อจำกัดนี้เอง Retail รุ่นก่อนหน้านี้จึงไม่สนับสนุนสถานการณ์จำลองที่ทำการแลกเปลี่ยนผลิตภัณฑ์โดยใช้เอกสารใบสั่งส่งคืนสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, functionality has been added to support scenarios where exchanges are done on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม มีการเพิ่มฟังก์ชันเพื่อรองรับสถานการณ์จำลองที่ทำการแลกเปลี่ยนผลิตภัณฑ์ในใบสั่งส่งคืนสินค้าแล้ว</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Retail now uses the sales order document instead of the return order document to process these types of transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ขณะนี้ Retail จึงใช้เอกสารใบสั่งขายแทนเอกสารใบสั่งส่งคืนสินค้าเพื่อประมวลผลธุรกรรมชนิดนี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Configure Retail to support exchanges on return orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่าคอนฟิก Retail ให้สนับสนุนการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to configure the system to support exchanges on return orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดำเนินการตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิกระบบให้สนับสนุนการแลกเปลี่ยนในใบสั่งส่งคืนสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไปที่ <bpt id="p1">**</bpt>การขายปลีก <ph id="ph1">\&gt;</ph> การตั้งค่าศูนย์ควบคุม <ph id="ph2">\&gt;</ph> พารามิเตอร์ <ph id="ph3">\&gt;</ph> พารามิเตอร์การขายปลีก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>On the <bpt id="p1">**</bpt>Customer orders<ept id="p1">**</ept> FastTab, set the <bpt id="p2">**</bpt>Process return orders as sales orders<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บนแท็บด่วน <bpt id="p1">**</bpt>ใบสั่งของลูกค้า<ept id="p1">**</ept> ตั้งค่าตัวเลือก <bpt id="p2">**</bpt>ประมวลผลใบสั่งส่งคืนสินค้าเป็นใบสั่งขาย<ept id="p2">**</ept> เป็น <bpt id="p3">**</bpt>ใช่<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Run the <bpt id="p1">**</bpt>Global configuration distribution schedule<ept id="p1">**</ept> job (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รันงาน <bpt id="p1">**</bpt>กำหนดการการกระจายการตั้งค่าคอนฟิกส่วนกลาง<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1110<ept id="p2">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Make an exchange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ทำการแลกเปลี่ยน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หลังจากตั้งค่าคอนฟิกระบบตามที่อธิบายไว้ในส่วนก่อนหน้าแล้ว ผู้ใช้การขายหน้าร้าน (POS) จะยังคงเลือกใบสั่งขายหรือใบแจ้งหนี้การขายเพื่อประมวลผลการส่งคืนเหมือนกับใน Retail เวอร์ชันก่อนหน้าได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ดี หลังจากเพิ่มสินค้ารับคืนไปยังรถเข็นแล้ว ผู้ใช้จะสามารถเพิ่มรายการขายใหม่ไปยังรถเข็นได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับรายการขายใหม่เหล่านี้ ผู้ใช้ต้องกำหนดแอตทริบิวต์ทั้งหมดที่จะเป็นเพื่อประมวลผลรายการใบสั่งของลูกค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>These attributes include the delivery method and fulfillment location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แอททริบิวต์เหล่านี้รวมถึงวิธีการจัดส่งและสถานที่สำหรับการเติมสินค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The payment that is due for the transaction will be a net of the return order lines and sales order lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การชำระเงินที่ครบกำหนดชำระสำหรับธุรกรรมจะเป็นเงินสุทธิของรายการใบสั่งส่งคืนสินค้าและรายการใบสั่งขาย</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อมีการชำระเงินสำหรับธุรกรรมดังกล่าวแล้ว ใบสั่งส่งคืนสินค้าจะได้รับการลงรายการบัญชีเป็นเอกสารใบสั่งขายใน Retail Headquarters และระบบจะออกใบแจ้งหนี้ให้กับรายการส่งคืนทันที</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อให้เห็นภาพยอดเงินต่างๆ สำหรับรถเข็นอย่างชัดเจนยิ่งขึ้น จึงมีการเพิ่มฟิลด์ยอดเงินใหม่ไปยังรถเข็น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can use the screen designer to make these new fields available in the POS user interface (UI).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถใช้ตัวออกแบบหน้าจอเพื่อทำให้ฟิลด์ใหม่เหล่านี้พร้อมใช้งานในอินเทอร์เฟสผู้ใช้ POS (UI)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Deposit applied<ept id="p1">**</ept> – The deposit amount that is applied on a transaction when the user does a customer order pickup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ใช้ยอดเงินฝากแล้ว<ept id="p1">**</ept> – ยอดเงินในการฝากเงินที่ใช้กับธุรกรรมเมื่อผู้ใช้เบิกสินค้าตามใบสั่งของลูกค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หากไม่มีการแทนที่เงินฝากและมีการตั้งค่าคอนฟิกเงินฝากที่ 10 เปอร์เซ็นต์ ยอดเงินในฟิลด์นี้จะเท่ากับ 90 เปอร์เซ็นต์ของยอดเงินรวมของใบสั่งลูกค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Carry out amount<ept id="p1">**</ept> – The total amount for lines where the delivery mode was set to <bpt id="p2">**</bpt>Carry out<ept id="p2">**</ept> when the customer order was created or edited, or during a customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ดำเนินการกับยอดเงิน<ept id="p1">**</ept> – ยอดเงินรวมของรายการที่มีการตั้งค่าวิธีการจัดส่งเป็น <bpt id="p2">**</bpt>ดำเนินการ<ept id="p2">**</ept> เมื่อสร้างหรือแก้ไขใบสั่งของลูกค้าหรือในระหว่างการแลกเปลี่ยนใบสั่งลูกค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ยอดเงินในฟิลด์นี้จะรวมภาษีและค่าธรรมเนียมไว้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Return amount<ept id="p1">**</ept> – The total amount for lines that have negative quantities during the customer order exchange.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ยอดส่งคืน<ept id="p1">**</ept> – ยอดเงินรวมสำหรับรายการที่มีปริมาณติดลบในระหว่างการแลกเปลี่ยนใบสั่งลูกค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The amount in this field includes taxes and charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ยอดเงินในฟิลด์นี้จะรวมภาษีและค่าธรรมเนียมไว้</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>