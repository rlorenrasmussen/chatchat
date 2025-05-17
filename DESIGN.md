# app summary
A chat app that has all the typical groupchat features, but it also has one-click accessible lists of pending TO-DOs for each member of the chat. The app is intended to harness gentle social pressure into helping people (particularly neurodivergent people) achieve their goals.

# features
## messaging
    - send/receive messages
    - reacting
    - scheduled send
    - multimedia/file-sharing
    - end-to-end encryption, obvi
    - a bot that can ping you about late tasks and ping your friends to cajole you
    - bi-directional linking to tasks & events
## tasks
    - contains
        - status (TODO, DOING, DONE)
        - title
        - description
        - "remind me" date
        - creator
        - ownership (you can only make tasks for yourself, but maybe it will be possible to have shared tasks)
        - stakes?
        - media
    - creating
    - viewing
    - editing
    - deleting
    - tagging
## calendar
    - show days/weeks/months
    - time starts on 9/11/2001 ((NEVER FORGET))
    - events
        - are these different from tasks?
        - title
        - description
        - date
        - time
        - attendees/participants
        - linked tasks??

# question marks
- networking???
    - centralized vs decentralized
    - literally how to send a message from one computer to another
        - without paying for hosting?
    - what is the furthest boundary i can establish around messaging that will be compatible with who-knows-what networking stuff?
- encryption
    - are there pre-existing libraries?
    - how should i tackle key generation? is that laid out with the libraries?
- storage
    - how to save to file in js?
    - do i need a database?
- prior art
    - should this just be a discord mod?

# modules
## viewer
- frame the message view (served by messenger)
- frame the task view (served by tasker)
- frame the plan view (served by planner)
## messenger
- serve the message view
- keep message history
- create messages to send
- send messages (via networker)
## tasker
- serve the task view
- keep task lists
- create tasks
## networker
- encrypt and packetize messages
- transmit messages over network
- receive messages over network
- depacketize and decrypt messages
## planner
- serve the plan view
- keep event list
- create/edit/delete events
## logger
- keep log entry list
- accept log entries
- report log entries (filter by level)