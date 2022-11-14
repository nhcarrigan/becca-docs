# Ticket System

Becca includes a system that allows your users to create private conversations with you and your team. [There are three settings](/configure-server#global-configurations) related to the ticket system, though only two must be set before users may create tickets.

## Ticket Category

> [!DANGER]
>
> In order to create new channels, Becca **must** have the `View Channels`, `Manage Channels`, and `Manage Permissions` explicitly allowed **on the category**. Otherwise, new tickets will fail to create.

The ticket category determines where new tickets will be created. Channels created in this category by Becca will be visible only to Becca, members with the `Administrator` permission, and the user who created the individual ticket.

## Ticket Log Channel

When a ticket is closed, Becca dumps a `.txt` file of all messages sent in that ticket. This channel determines where she should upload that log, so that your team can refer to it at a future date if needed.

## Ticket Role

If desired, you can configure a specific role (such as a moderator role) to be automatically added to all new tickets. This allows you to have your support team assist with ticket handling, without having to grant administrator permissions.
