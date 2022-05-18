# Recommendations
<!--
Intave does not set the trust factor by itself. <br>
You will have to - either with [intave/access](https://github.com/intave/access) or with good old permissions,
otherwise we will just assign the 🟧 Orange Trust Factor or a different given default.<br>

## What trustfactor should I set?
-->
Give **high-level**, **long-time-playing** and **trusted** players a 🟨 Yellow Trust Factor.<br>
Only give a 🟩 Green Trust Factor to players you **trust blindly** - for example your **staff members**, **yourself** and
players with something like the client-side **Badlion AntiCheat** enabled.<br>
If a player's Ip-Address has been banned recently or is similar to a banned Ip-Address' Subnet, set a 🟥 Red or a 
Dark-Red Trust Factor.<br>
If you have Bedrock players on your server, give them the :white_large_square: White Trust Factor. Minecraft Bedrock
significantly changes the protocol and would get flagged otherwise.

::: danger
1. **Don't show players their trust factor**, as this would allow for trustfactor mapping reverse-engineering.<br>
2. **Don't publish your trust factor mappings/code**, as it would allow for trustfactor reverse-engineering<br>
3. **Avoid giving new players a high (🟨 Yellow, 🟩 Green, :white_large_square: White) trustfactor**<br>
:::

## Indicators for trust
Any interaction with your server that requires time or money, like player ranks and playtime, is by our means considered
a good indicator for trust. Best if you combine the two factors - e.g. `100h playtime or (50h playtime and rank)`.

A player with a rank-purchase and an overall (non-afk) playtime of over 50 hours can be considered an active, trusted
player.<br>
While in theory cheaters could get ranks and a lot of playtime, most of them just don't bother investing hours into an account, which they usually don't even keep for long.
When banned, you would require them to play another X hours and get another rank, just to abuse trust factor advantages.

::: tip
You might want to take chargebacks/refunds into account, a purchase that can arbitrarily be refunded is a questionable trust indicator.<br>
:::
## Indicators for distrust
Any irregular context a player is in (like a recent ban on the players ip) can be used to assign a lower
trustfactor.<br>
Servers not requiring Mojang-authenticated accounts might consider players without proper authentication suspicious.
::: tip
In [intave/access](https://github.com/intave/access), you can use
[TrustFactor.unsafer()](https://github.com/intave/access/blob/e212600accd7aa647fe812a586f298ce4cf7d7eb/src/main/java/de/jpx3/intave/access/player/trust/TrustFactor.java#L33)
to lower a trust factor
:::