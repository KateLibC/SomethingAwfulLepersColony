Something Awful Lepers Colony Data
==================================

This JSON file (`data.json`) contains all ban, probation, and permaban detail
from August 7th, 2004 through to September 9th, 2015. The data is not provided
in a sorted format but timestamps are provided.

The data was sourced from the following URL:
http://forums.somethingawful.com/banlist.php

To read the data, treat each entry from the `data` key as per the following example
code:

    {
        "CleanComment": "No no no no no.  User loses posting privileges for 6 hours.",
        "TargetUserID": 106021,
        "ModApproverName": "Squeezy Farm",
        "BanLength": 21600,
        "EventTime": 1441807980,
        "ModRequestorName": "Squeezy Farm",
        "RawComment": "Tm8gbm8gbm8gbm8gbm8uICBVc2VyIGxvc2VzIHBvc3RpbmcgcHJpdmlsZWdlcyBmb3IgNiBob3Vycy4=",
        "BanType": "probation",
        "ModRequestorID": 152981,
        "TargetUserName": "Bill Dungsroman",
        "PostID": 449978584,
        "ModApproverID": 152981
    },

Each of the following keys in each item in the list can be treated as the
following:

* `CleanComment` - this is a remark made by the requesting moderator. This has
had the data sanitised so it should not contain any HTML.
* `TargetUserID` - the user ID for the user that has had the punishment
inflicted upon.
* `ModApproverName` - name of the moderator that approved the punishment
request.
* `BanLength` - time in seconds for how long the probation will last. This will
remain as null should it not be parsed successfully from the comment.
* `EventTime` - event in epoch time (set to UTC) when this action occurred.
* `ModRequestorName` - name of the moderator that requested the punishment.
* `RawComment` - this is the comment before it was cleansed. This has been
encoded in base 64 to prevent any complications with some JSON parsers.
* `BanType` - set to either 'ban', 'permaban', or 'probation'.
* `ModRequestorID` - user ID of the moderator that requested the punishment.
* `TargetUserName` - the username of the account being punished.
* `PostID` - post ID resulting in the account punishment. This may be set to
null.
* `ModApproverID` - the user ID of the moderator that approved the action.

Other than that you may need to run some checks on the keys just in case there
is a null value in lieu of what may be a string or integer.

The data is provided as is so please do not complain if something is missing
or there are problems with the data.
