# Håndbok N801 \(SIRI/NeTEX\) : SIRI-SX - Validity of a message

**Content**

**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591774160 {padding: 0px;}  
div.rbtoc1619591774160 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591774160 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/**

* [**Limited validity already when published**](handbok-n801-siri-netex-siri-sx-validity-of-a-message.md#SIRI-SX-Validityofamessage-Limitedvalidityalreadywhenpublished)
* [**Valid until a new message closes the initial message**](handbok-n801-siri-netex-siri-sx-validity-of-a-message.md#SIRI-SX-Validityofamessage-Validuntilanewmessageclosestheinitialmessage)
  * [**EndTime must be defined in the "closing" message**](handbok-n801-siri-netex-siri-sx-validity-of-a-message.md#SIRI-SX-Validityofamessage-EndTimemustbedefinedinthe%22closing%22message)

XML

See complete examples:

* Tidsbegrenset melding:  [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-timebound.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-timebound.xml)
* Åpen melding:  [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-open-ended.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-open-ended.xml)
* Lukking av åpen melding:  [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-close.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-close.xml)

## Limited validity already when published <a id="SIRI-SX-Validityofamessage-Limitedvalidityalreadywhenpublished"></a>

The message is visible to the public and in real-time data streams up to the time defined in `<EndTime>`.

```text
<Progress>open</Progress>
<ValidityPeriod>
	<StartTime>2018-02-11T11:33:11</StartTime>
	<EndTime>2018-04-22T22:55:00</EndTime>
</ValidityPeriod>
```

## Valid until a new message closes the initial message <a id="SIRI-SX-Validityofamessage-Validuntilanewmessageclosestheinitialmessage"></a>

The message is visible to the public and in real-time data streams from the time defined in `<StartTime>` until an updated of the message \(with the same ID\) changes `<Progress>` from 'open' to 'closed.**Uten sluttid**

```text
<Progress>open</Progress>
<ValidityPeriod>
	<StartTime>2018-02-11T11:33:11</StartTime>
</ValidityPeriod>
```

### EndTime must be defined in the "closing" message <a id="SIRI-SX-Validityofamessage-EndTimemustbedefinedinthe&quot;closing&quot;message"></a>

When the status of a message changes from 'open' to 'closed', EndTime of the message must be set to **at least 5 hours into the future**. This is to ensure that all systems are able to receive the close-message, even when there are severe disturbances in uptime.**Sluttid**

```text
<Progress>closed</Progress>
<ValidityPeriod>
	<StartTime>2018-02-11T11:33:11</StartTime>
	<EndTime>2018-02-12T20:10:00</EndTime>
</ValidityPeriod>
```

When `<Progress>closed</Progress>` is received, the message will:

* not be shown in search results in the journey planner.
* be available with `<Progress>closed</Progress>` in real-time streams until the `<EndTime>` has passed.

