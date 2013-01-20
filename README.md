{
    "name": "SSBB",
    "author": ["Hoboman2.0","RiceKirby"],
    "summary": "Nintendo's all-stars collide in a wild and crazy mafia theme, in this one Brawl to end them all! No brawler is safe at any moment, be it mafia or villager... Created by Hoboman2.0, PM him if you want to leave any comments and suggestions. Changelog: Zelda is on Ganondorfs team BTW. New Challenger: Lucario, he can use /inspect to find out what team someone is on! /taunt on snake changed to a night action, /stalk!  ZSS implemented. Game and Watch is in. He is the spiritual replacement to the slot that Ice Climbers had. SSBB has also been played over 3000 Times! RiceKirby now can also alter stuff! TODO: Give Lucario and Link more interesting stuffs, and finally finish Yoshi. Also, make the most awesomest Kirby EVAR!",
    "border": "***~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~^~",
    "sides": [
        {
            "side": "mafia",
            "translation": "Koopa",
            "winmsg": "And the winner is... Bowser! (~Players~)!!"
        },
        {
            "side": "mafia1",
            "translation": "Hyrulian Mafia",
            "winmsg": "And the winner is... The Hyrulian Mafia (~Players~)!"
        },
        {
            "side": "Meta Knight",
            "translation": "Meta Knight",
            "winmsg": "<Cue epic music> And the winner is... Meta Knight! (~Players~)"
        },
        {
            "side": "mafia2",
            "translation": "Italian Mafia",
            "winmsg": "And the winner is... The Italian Mafia!! (~Players~)!"
        },
        {
            "side": "mafia3",
            "translation": "Penguin Mafia",
            "winmsg": "And the winner is... King Dedede (~Players~)!"
        },
        {
            "side": "Ice Climbers",
            "translation": "Ice Climbers",
            "winmsg": "And the winner is... Ice Climbers(~Players~)!"
        },
        {
            "side": "village",
            "translation": "Good people",
            "winmsg": "And the winner is... The Village(~Players~)!"
        },
        {
            "side": "Wolf",
            "translation": "Wolf",
            "winmsg": "And the winner is... Wolf(~Players~)!"
        },
        {
            "side": "godfather",
            "translation": "Purin",
            "winmsg": "And thus began Jigglypuff's(~Players~) 1000 year Reign of Terror over Humanity. May Arceus help you all."
        },
        {
            "side": "G&W",
            "translation": "Game & Watch",
            "winmsg": "Mr. Game & Watch(~Players~), pities all of the fools he trampled over to achieve glorious victory this round!"
        }
    ],
    "roles": [
        {
            "role": "villager",
            "translation": "Mario",
            "side": "village",
            "help": "You are Mario! If you don't know who he is, get out from under your rock! You don’t have any special commands during the night, but you do have a tiny chance to find out who is going to be killed! Vote to remove people in the day!",
            "actions": {
                "hax": {
                    "kill": {
                        "revealTeam": 0.07,
                        "revealPlayer": 0.04
                    },
                    "poison": {
                        "revealTeam": 0.06,
                        "revealPlayer": 0.05
                    }
                }
            }
        },
        {
            "role": "sonic",
            "translation": "Sonic",
            "side": "village",
            "help": "You are Sonic the Hedgehog, the fastest thing alive! You have a 70% chance of evading kills, a 60% chance of evading poison, and if the kill is a daykill, you even survive! However, due to being so annoying, you vote counts as 0. You can also use /taunt, to reveal yourself as Sonic during the standby phase!",
            "actions": {
                "vote": 0,
                "kill": {
                    "mode": {
                        "evadeChance": 0.7
                    }
                },
                "poison": {
                    "mode": {
                        "evadeChance": 0.6
                    }
                },
                "standby": {
                    "taunt": {
                        "command": "reveal",
                        "revealmsg": "~Self~ (~Role~) runs around everyone screaming 'YOU'RE TOO SLOW!'."
                    }
                },
                "daykill": "revenge"
            }
        },
        {
            "role": "luigi",
            "translation": "Luigi",
            "side": "village",
            "help": "You are Luigi, King of Second Bananas! You don’t have any special commands during the night! Oh, and your vote counts as -1!",
            "actions": {
                "vote": -1,
                "startup": "role-reveal"
            }
        },
        {
            "role": "inspector",
            "translation": "Lucas",
            "side": "village",
            "help": "You are Lucas, amazing PSI extrodinare. Type /inspect [name] to find his/her identity! Due to being a minor, you vote only counts for .5 though! You also have a 1/2 chance of evading Daykills!",
            "actions": {
                "vote": 0.5,
                "daykill": {
                    "mode": {
                        "evadeChance": 0.5
                    }
                },
                "night": {
                    "inspect": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 30
                    }
                }
            }
        },
        {
            "role": "ness",
            "translation": "Ness",
            "side": "village",
            "help": "You are Ness, PSI extrodinare from Eagleland! Because of your mastery of PSI, you can type /protect [name] to protect someone! You can also use /safeguard [name] to protect someone against poison, although it also protects against inspect and distract! PSI also allows you have a small chance of finding out who gets killed next!(No action). Your vote counts for .5 though, due to being a minor, but you have a voteshield of 3(if voted for, it takes 3 more votes to remove you)!,",
            "actions": {
                "vote": 0.5,
                "voteshield": -3,
                "night": {
                    "protect": {
                        "target": "AnyButSelf",
                        "common": "Role",
                        "priority": 4,
                        "broadcast": "role"
                    },
                    "safeguard": {
                        "target": "AnyButSelf",
                        "common": "Role",
                        "priority": 6,
                        "broadcast": "role"
                    }
                },
                "hax": {
                    "kill": {
                        "revealTeam": 0.3,
                        "revealPlayer": 0.1
                    }
                }
            }
        },
        {
            "role": "bodyguard",
            "translation": "Donkey Kong",
            "side": "village",
            "help": "You are Donkey Kong, fairly huge ape! Type /protect [name] to protect someone! You can protect two people, due to your giant size. Because you are an ape, you are immune to distraction!",
            "actions": {
                "night": {
                    "protect": {
                        "target": "AnyButSelf",
                        "common": "Role",
                        "priority": 5,
                        "broadcast": "role",
                        "limit": 2
                    }
                },
                "startup": "role-reveal",
                "distract": {
                    "mode": "ignore",
                    "msg": "The ~Distracter~ came to you last night! You ignored her!"
                }
            }
        },
        {
            "role": "smallBG",
            "translation": "Donkey Kong",
            "side": "village",
            "help": "You are Donkey Kong, fairly huge ape! Type /protect [name] to protect someone! Because you are an ape, you are immune to distraction!",
            "actions": {
                "night": {
                    "protect": {
                        "target": "AnyButSelf",
                        "common": "Role",
                        "priority": 5,
                        "broadcast": "role"
                    }
                },
                "startup": "role-reveal",
                "distract": {
                    "mode": "ignore",
                    "msg": "The ~Distracter~ came to you last night! You ignored her!"
                }
            }
        },
        {
            "role": "mafia",
            "translation": "Bowser",
            "side": "mafia",
            "help": "You are Bowser, Koopa King, and eternal nemesis of Mario! Type /kill [name] to kill someone!",
            "actions": {
                "night": {
                    "kill": {
                        "target": "AnyButTeam",
                        "common": "Team",
                        "priority": 11,
                        "broadcast": "team"
                    }
                },
                "startup": "team-reveal"
            }
        },
        {
            "role": "werewolf",
            "translation": "Wolf",
            "side": "Wolf",
            "help": "You are Wolf, the dude who can't let Star Fox do stuff! Type /kill [name] to kill someone! In addition, if you get distracted, you will kill them instead!",
            "actions": {
                "night": {
                    "kill": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 9
                    }
                },
                "distract": {
                    "mode": "ChangeTarget",
                    "hookermsg": "You tried to distract Wolf (what an idea, srsly), you were ravishly shot at!",
                    "msg": "The ~Distracter~ came to you last night! You devoured her instead !"
                },
                "avoidHax": [
                    "kill"
                ]
            }
        },
        {
            "role": "hooker",
            "translation": "Peach",
            "side": "village",
            "help": "You are Peach, Princess of the Mushroom Kingdom! Type /distract [name] to distract someone! Vote to remove people in the day! Due to being a princess, your vote counts as 2!",
            "actions": {
                "vote": 2,
                "night": {
                    "distract": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 1
                    }
                }
            }
        },
        {
            "role": "mayor",
            "translation": "Captain Falcon",
            "side": "village",
            "help": "You are Captain Falcon, F-Zero Racer! You dont have any special commands during the night. Vote to remove people in the day, your vote counts as 3, because YOU ARE A FREAKING CAPTAIN! Use /punch [name] to remove people with a falcon punch during standby! You will be revealed.",
            "actions": {
                "vote": 3,
                "standby": {
                    "punch": {
                        "target": "AnyButSelf",
                        "msg": "You can kill now using /punch [name] :",
                        "killmsg": "~Self~ pulls out a fist and punches it through ~Target~'s chest! FALCON PAUWNCH!",
                        "command": "kill"
                    }
                }
            }
        },
        {
            "role": "spy",
            "translation": "Snake",
            "side": "village",
            "help": "You are Solid Snake, commando of FOXHOUND! You can find out who is going to get killed or poisoned or inspected next!(no command for this ability) Vote to remove people in the day! You can use /stalk to tell who someone visited during the night! Due to your uber stealth skills, You have a 20% chance of evading kills(No command for this)!",
            "actions": {
                "kill": {
                    "mode": {
                        "evadeChance": 0.2
                    }
                },
                "night": {
                    "stalk": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 1
                    }
                },
                "hax": {
                    "kill": {
                        "revealTeam": 0.35,
                        "revealPlayer": 0.15
                    },
                    "poison": {
                        "revealTeam": 0.25,
                        "revealPlayer": 0.15
                    },
                    "inspect": {
                        "revealTeam": 0.2,
                        "revealPlayer": 0.1
                    }
                }
            }
        },
        {
            "role": "godfather",
            "translation": "Jigglypuff",
            "side": "godfather",
            "help": "You are Jigglypuff, the balloon Pokémon! Type /rest [name] to kill someone! You can kill 2 targets, Type /rest [name2] again to select your second target! Your vote also counts as 2.",
            "actions": {
                "vote": 2,
                "night": {
                    "rest": {
                        "command": "kill",
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 21,
                        "limit": 2
                    }
                },
                "distract": {
                    "mode": "ChangeTarget",
                    "hookermsg": "You tried to seduce the Marshmallow, you were rested when you least expected it!",
                    "msg": "The ~Distracter~ came to you last night! You killed her instead!"
                },
                "avoidHax": [
                    "kill"
                ]
            }
        },
        {
            "role": "vigilante",
            "translation": "Link",
            "side": "village",
            "help": "You are Link! Who knows which one though... Type /kill [name] to kill someone using the Master Sword! You can also, once per game, reveal someone's identity during the standby phase (don't kill the good people, and please, do not kill randomly)",
            "actions": {
                "night": {
                    "kill": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 19
                    }
                },"standby":{
  	"expose": {
                        "target": "AnyButSelf",
                        "msg": "You can type /expose [name] to reveal someone's role!",
                        "exposemsg": "~Self~ (Link) uses the Lens of Truth, and announces to everyone that ~Target~ is the ~Role~!",
		       "recharge":9999

		
}}
            }
        },
       
 {
            "role": "samus",
            "translation": "Samus",
            "side": "village",
            "help": "You are the amazing bounty hunter, Samus Aran! Type /kill [name] to kill someone using a missile! (don't kill the good people!) Type /distract [name] to distract someone! You can only distract every other turn! Due to your ability to escape with your MorphBall, you have a 10% chance of dodging kills. Also, due to your bulky powersuit, you have a 50% chance of avoiding poison!(No command for avoiding/dodging)! You can also change to Zero Suit Samus using /change, who can /distract every turn, but can only kill every other turn, and has a 50% chance of dodging kills, but a 10% chance of dodging poison!",
            "actions": {
                "kill": {
                    "mode": {
                        "evadeChance": 0.1
                    }
                },
                "poison": {
                    "mode": {
                        "evadeChance": 0.5
                    }
                },
                "night": {
                    "kill": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 20
                    },
                    "distract": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 2,
"recharge":2
                    },
			"change":{
"canConvert": [ "samus"
                  ],

                        "newRole": "ZSS",
                        "target": "OnlySelf",
                        "common": "Self",
                        "command": "convert",
                        "priority": 1,
                        "recharge": 2,
		      "convertmsg":"+Snake: Samus took her clothes off!"
                    }

                }
            }
        },{
            "role": "ZSS",
            "translation": "ZSS",
            "side": "village",
            "help": "Ya-de-daa-de-daa. NULL STUFF!",
            "actions": {
                "kill": {
                    "mode": {
                        "evadeChance": 0.5
                    }
                },
                "poison": {
                    "mode": {
                        "evadeChance": 0.1
                    }
                },
                "night": {
                    "kill": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 20,
	"recharge":2
                    },
                    "distract": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 2
                    },"change":{
"canConvert": [ "ZSS"
                  ],

                        "newRole": "samus",
                        "target": "OnlySelf",
                        "common": "Self",
                        "command": "convert",
                        "priority": 1,
                        "recharge": 2,
		      "convertmsg":"Samus put her Suit back on!"
                    }
                }
            }
        },
         {
            "role": "mafia1",
            "translation": "Ganondorf",
            "side": "mafia1",
            "help": "You are Ganondorf, the King of Evil! Type /kill [name] to kill someone!",
            "actions": {
                "night": {
                    "kill": {
                        "target": "AnyButTeam",
                        "common": "Team",
                        "priority": 12,
                        "broadcast": "team"
                    }
                },
                "startup": "team-reveal-with-roles"
            }
        },
        {
            "role": "mafia2",
            "translation": "Wario",
            "side": "mafia2",
            "help": "You are Wario, the rather chubby Anti-Mario! Type /poison [name] to poison someone, which causes them die next night! You also have a slight chance of discovering people who have the protect command!",
            "actions": {
                "night": {
                    "poison": {
                        "target": "AnyButTeam",
                        "common": "Team",
                        "priority": 11,
                        "broadcast": "team",
                        "poisonDeadMessage": "You got killed by the poison of Wa-Wa-Wario!"
                    }
                },
                "hax": {
                    "protect": {
                        "revealPlayer": 0.1
                    }
                },
                "startup": "team-reveal-with-roles"
            }
        },
        {
            "role": "mafiaboss2",
            "translation": "Wario Man",
            "side": "mafia2",
            "help": "You are Wario Man, Wario's Alter Ego! Type /kill [name] to kill someone! Type /poison [name] to poison someone, and they will die the following night, and this goes through protect!",
            "actions": {
                "night": {
                    "poison": {
                        "target": "AnyButTeam",
                        "common": "Team",
                        "priority": 11,
                        "broadcast": "team",
                        "poisonDeadMessage": "You got killed by the poison of Wa-Wa-Wario!"
                    },
                    "kill": {
                        "target": "AnyButTeam",
                        "common": "Self",
                        "priority": 10,
                        "broadcast": "team"
                    }
                },
                "startup": "team-reveal"
            }
        },
        {
            "role": "mafia3",
            "translation": "King Dedede",
            "side": "mafia3",
            "help": "You are King Dedede, the greedy king of Dreamland! Type /kill [name] to kill someone! Your vote counts for 4",
            "actions": {
                "vote": 4,
                "night": {
                    "kill": {
                        "target": "AnyButTeam",
                        "common": "Self",
                        "priority": 13,
                        "broadcast": "Team"
                    }
                },
                "startup": "team-reveal-with-roles"
            }
        },
        {
            "role": "mafia3b",
            "translation": "WaddleDoo",
            "side": "mafia3",
            "help": "You are a WaddleDoo, the rather innocent servernt of the greedy king of Dreamland! Type /protect [name] to protect someone(Hint: Protect Dedede, or Meta Knight!). You also evade daykills due to being inconspicuous, and inspections reveal you as an innocent Mario, due to being pure of heart! Your vote counts for .5, due to being a servent!",
            "actions": {
                "vote": 0.5,
                "night": {
                    "protect": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 7,
                        "broadcast": "Team"
                    }
                },
                "inspect": {
                    "revealAs": "villager"
                },
                "startup": "team-reveal-with-roles",
                "daykill": "evade"
            }
        },
        {
            "role": "Olimar",
            "translation": "Olimar",
            "side": "village",
            "help": "You are Olimar, Employee of the Hocotate Freights. Due to the multitude of pikmin, you have a vote of 6! Also, due to your space suit, you are immune to poison!",
            "actions": {
                "vote": 6,
                "poison": {
                    "mode": "ignore"
                }
            }
        },
        {
            "role": "mafiaboss1",
            "translation": "Ganon",
            "side": "mafia1",
            "help": "You are Ganon, the great big beast that resides within Ganondorf! Type /kill [name] to kill someone! You avoid kills made during the day! You can't be distracted!",
            "actions": {
                "night": {
                    "kill": {
                        "target": "AnyButTeam",
                        "common": "Team",
                        "priority": 12,
                        "broadcast": "team"
                    }
                },
                "distract": {
                    "mode": "ignore",
                    "msg": "The ~Distracter~ came to you last night! She barely escaped! Bwa. Hah. Hah. HAAAAA!"
                },
                "startup": "team-reveal",
                "daykill": "evade"
            }
        },
        {
            "role": "Meta Knight",
            "translation": "Meta Knight",
            "side": "Meta Knight",
            "help": "You are Meta Knight, the honorable and badass mysterious captain of the Halberd, and Type /kill [name] during the day phase to kill someone! You will not be revealed when you kill! You are allied with yourself! Due to being a badass, your vote is 1.5!",
            "actions": {
                "vote": 1.5,
                "standby": {
                    "kill": {
                        "target": "AnyButSelf",
                        "msg": "You can kill now using /kill [name] :",
                        "killmsg": "Meta Knight pulls out the holy sword, Galaxia, and strikes it through ~Target~'s chest!"
                    }
                }
            }
        },
        {
            "role": "Meta Knight2",
            "translation": "Meta Knight",
            "side": "mafia3",
            "help": "You are Meta Knight, the honorable and badass mysterious captain of the Halberd, and Type /kill [name] during the day phase to kill someone! You will not be revealed when you kill! You are allied with King Dedede!",
            "actions": {
                "startup": "team-reveal-with-roles",
                "standby": {
                    "kill": {
                        "target": "AnyButSelf",
                        "msg": "You can kill now using /kill [name] :",
                        "killmsg": "Meta Knight pulls out the holy sword, Galaxia, and strikes it through ~Target~'s chest!"
                    }
                }
            }
        },
        {
            "role": "samurai",
            "translation": "Marth",
            "side": "village",
            "help": "You are Marth, king of Altea! Type /kill [name] during the day phase to kill someone! You will not be revealed when you kill! You are allied with the Good people.",
            "actions": {
                "standby": {
                    "kill": {
                        "target": "AnyButSelf",
                        "msg": "You can kill now using /kill [name] :",
                        "killmsg": "Marth pulls out a sword and strikes it through ~Target~'s chest! Critical Hit!",
                        "revealchance": 0.33,
                        "revealmsg": "±Game: After using Critical Hit, Marth tripped (Sakurai!!!!!), and was revealed to be ~Self~!"
                    }
                }
            }
        },
        {
            "role": "miller",
            "translation": "Kirby",
            "side": "village",
            "help": "You are Kirby! You don’t have any special commands during the night! Vote to remove people in the day! You probably should't have inhaled Bowser earlier, because now Lucas sees you as mafia!",
            "actions": {
                "inspect": {
                    "revealAs": "mafia"
                }
            }
        },
        {
            "role": "IceClimbers",
            "translation": "Ice Climbers",
            "side": "Ice Climbers",
            "help": "You are the Ice Climbers. You are two people, technically! Your vote counts as 2 during the day! You can /kill [name] to kill someone during the night! You can /distract [name] to distract someone during the night! You also have a 20% chance of evading kills, and a 30% chance of evading poison! Vote to remove people in the day!",
            "actions": {
                "night": {
                    "kill": {
                        "common": "Self",
                        "target": "AnyButSelf",
                        "priority": 16
                    },
                    "distract": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 8
                    }
                },
                "poison": {
                    "mode": {
                        "evadeChance": 0.3
                    }
                },
                "kill": {
                    "mode": {
                        "evadeChance": 0.2
                    }
                },
                "vote": 2
            }
        },
        {
            "role": "inspector2",
            "translation": "Lucario",
            "side": "village",
            "help": "You are Lucario, the Aura Pokémon! Type /inspect [name] to find what team that person is!",
            "actions": {
                "night": {
                    "inspect": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 31,
                        "Sight": "Team"
                    }
                }
            }
        },
        {
            "role": "miller2",
            "translation": "Pit",
            "side": "village",
            "help": "You dont have any special commands during the night! Vote to remove people in the day!",
            "actions": {
                "inspect": {
                    "revealAs": "Meta Knight"
                },
                "lynch": {
                    "revealAs": "miller2"
                },
                "startup": {
                    "revealAs": "villager"
                },
                "onlist": "Meta Knight"
            }
        },
        {
            "role": "M1hooker",
            "translation": "Zelda",
            "side": "mafia1",
            "help": "You are Zelda, Princess of Hyrule! You are sided with Ganondorf, because you are being possessed by Ganondorf! Type /distract [name] to distract someone! Vote to remove people in the day! Due to being a princess, your vote counts as 2!",
            "actions": {
                "vote": 2,
                "startup": "team-reveal-with-roles",
                "night": {
                    "distract": {
                        "target": "AnyButTeam",
                        "common": "Self",
                        "priority": 1
                    }
                }
            }
        },
        {
            "role": "G&W",
            "translation": "Mr. G&W",
            "side": "G&W",
            "help": "You are Mr. G&W, Resident of Flat Zone(Not to be confused with FlatLand). You can poison(/poison [Name]) someone during the night, and they will die two nights later! You can also kill someone every third night(/kill [Name])! You are sided with yourself! Also, those who kill you will be poisoned, and will die in four turns! You also have a vote of 2!",
            "actions": {"vote":2,
                "kill": {
                    "mode": "poisonattacker",
                    "count": 4,
                    "poisonDeadMessage": "You died from Mr. Game & Watch's Flit Gun!"
                },
                "night": {
                    "poison": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 14,
                        "poisonDeadMessage": "You have succumbed from the Toxic Air made by Mr. Game & Watch's Flit Gun!",
                        "count": 3
                    },
                    "kill": {
                        "target": "AnyButSelf",
                        "common": "Self",
                        "priority": 15,
                        "recharge": 3
                    }
		
                }
            }
        },
        {
            "role": "yoshi",
            "translation": "Yoshi",
            "help": "Yeah, I will eventually get to this, anyway, Knows marios, gets a bit of hax, and can use safeguard.",
            "side": "village",
            "actions": {
                "startup": {
                    "revealRole": "villager"
                },
                "night": {
                    "safeguard": {
                        "target": "AnyButSelf",
                        "common": "Role",
                        "priority": 3,
                        "broadcast": "role"
                    }
                }
            }
        }
    ],
    "roles1": [
        "smallBG",
        "mafia",
        "inspector",
        "werewolf",
        "hooker",
        "villager",
        "mafia",
        "villager",
        "miller",
        "villager",
        "mayor"
    ],
    "roles2": [
        "bodyguard",
        "mafia1",
        "mafia1",
        "inspector",
        "hooker",
        "villager",
        "mafia2",
        "luigi",
        "luigi",
        "mayor",
        "villager",
        "Meta Knight",
        "spy",
        "mafia2",
        "mafia3",
        "ness",
        "villager",
        "luigi",
        "mafiaboss2",
        "sonic",
        "vigilante",
        "mafia3b"
    ],
    "roles3": [
        "bodyguard",
        "mafia1",
        "mafia1",
        "inspector",
        "hooker",
        "villager",
        "mafia2",
        "luigi",
        "luigi",
        "mayor",
        "villager",
        "Meta Knight2",
        "spy",
        "mafia2",
        "mafia3",
        "ness",
        "villager",
        "luigi",
        "mafiaboss2",
        "sonic",
        "vigilante",
        "mafia3b",
        "samus",
        "mafiaboss1",
        "miller2",
	"G&W",
        "inspector2",
	"villager",
"M1hooker",
        "mafia2",
        "samurai",
	"Olimar",
        "IceClimbers",
        "villager",
        "luigi",
	"godfather",
        "mafia3b",
        "werewolf",
        "luigi",
        "villager",
        "mafia1",
        "luigi",
        "villager"
    ],
    "villageCantLoseRoles": [
        "sonic",
        "mayor",
        "vigilante",
        "samurai",
        "samus",
        "hooker",
        "Olimar"
    ],
    "killmsg": "+Announcer: ~Player~(~Role~) has been thrown off of the screen!",
    "killusermsg": "You have been thrown off the screen!"
}
