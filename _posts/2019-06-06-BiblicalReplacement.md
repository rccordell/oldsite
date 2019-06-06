---
title: "Biblical Find & Replace"
date: 2019-06-06
author: Ryan Cordell
permalink: /teaching/biblicalreplacement/
layout: post
---

In my post/talk ["Teaching Humanities Data Analysis"](https://ryancordell.org/research/teachingHDA/) I recommended that such instruction start with creativity, and cited as an example an exercise I do with students designing mad-libs style Twitter poetry bots. The question of teaching data analysis is very much on my mind as I prepare the code workbooks that will serve as lessons for the "Introduction to Humanities Data Analysis & Visualization in R" I will teach with [Gregory J. Palermo](https://palermog.github.io/) at the [Digital Humanities Summer Institute](http://dhsi.org/index.php) next week. 

This morning I came across a Facebook post by [Lee Skallerup Bessette](https://readywriting.org/) linking to Daniel Mallory Ortberg's hilarious ["Bible Verses Where “Behold” Has Been Replaced With “Look, Buddy”](http://the-toast.net/2016/06/06/bible-verses-where-behold-has-been-replaced-with-look-buddy/), which gave me an idea for a fun, simple, day one exercise that will teach the very basics of filtering textual data and manipulating strings. Essentially, I wrote a short R function that accepts two strings—a phrase to search, and a phrase to replace it with—searches the King James Version of the Bible for all verses including the search phrase, and creates a news version of that verse using the replacement phrase. It works just like the `find and replace` functions in a program like Word, but with the slight advantage of only outputting the verses that include the replaced phrase. The pertinent code can be found in [this Gist on Github](https://gist.github.com/rccordell/ceb46023066b632a31d2c47d4b07369f). Please play around with it!

<script src="https://gist.github.com/rccordell/ceb46023066b632a31d2c47d4b07369f.js"></script>

To really come up with funny results, you have to be thoughtful about all of the contexts in which a given word or phrase are used, so that the substitution will be grammatically appropriate in each substitution. So, subbing "for real, dude," for "verily" works in nearly every instance:

```
Genesis 42:21 and they said one to another, we are for real, dude, guilty concerning our brother, in that we saw the anguish of his soul, when he besought us, and we would not hear; therefore is this distress come upon us.

Exodus 31:13 speak thou also unto the children of israel, saying, for real, dude, my sabbaths ye shall keep: for it is a sign between me and you throughout your generations; that ye may know that i am the lord that doth sanctify you.

Judges 15:2 and her father said, i for real, dude, thought that thou hadst utterly hated her; therefore i gave her to thy companion: is not her younger sister fairer than she? take her, i pray thee, instead of her.

1 Kings 1:43 and jonathan answered and said to adonijah, for real, dude, our lord king david hath made solomon king.

2 Kings 4:14 and he said, what then is to be done for her? and gehazi answered, for real, dude, she hath no child, and her husband is old.

1 Chronicles 21:24 and king david said to ornan, nay; but i will for real, dude, buy it for the full price: for i will not take that which is thine for the lord, nor offer burnt offerings without cost.

Job 19:13 he hath put my brethren far from me, and mine acquaintance are for real, dude, estranged from me.

Psalms 37:3 trust in the lord, and do good; so shalt thou dwell in the land, and for real, dude, thou shalt be fed.

Psalms 39:5 behold, thou hast made my days as an handbreadth; and mine age is as nothing before thee: for real, dude, every man at his best state is altogether vanity. selah.

Psalms 58:11 so that a man shall say, for real, dude, there is a reward for the righteous: for real, dude, he is a god that judgeth in the earth.

Psalms 66:19 but for real, dude, god hath heard me; he hath attended to the voice of my prayer.

Psalms 73:13 for real, dude, i have cleansed my heart in vain, and washed my hands in innocency.

Isaiah 45:15 for real, dude, thou art a god that hidest thyself, o god of israel, the saviour.

Jeremiah 15:11 the lord said, for real, dude, it shall be well with thy remnant; for real, dude, i will cause the enemy to entreat thee well in the time of evil and in the time of affliction.

Matthew 5:18 for for real, dude, i say unto you, till heaven and earth pass, one jot or one tittle shall in no wise pass from the law, till all be fulfilled.

Matthew 5:26 for real, dude, i say unto thee, thou shalt by no means come out thence, till thou hast paid the uttermost farthing.

Matthew 6:2 therefore when thou doest thine alms, do not sound a trumpet before thee, as the hypocrites do in the synagogues and in the streets, that they may have glory of men. for real, dude, i say unto you, they have their reward.

Matthew 6:5 and when thou prayest, thou shalt not be as the hypocrites are: for they love to pray standing in the synagogues and in the corners of the streets, that they may be seen of men. for real, dude, i say unto you, they have their reward.

Matthew 6:16 moreover when ye fast, be not, as the hypocrites, of a sad countenance: for they disfigure their faces, that they may appear unto men to fast. for real, dude, i say unto you, they have their reward.

Matthew 8:10 when jesus heard it, he marvelled, and said to them that followed, for real, dude, i say unto you, i have not found so great faith, no, not in israel.

Matthew 10:15 for real, dude, i say unto you, it shall be more tolerable for the land of sodom and gomorrha in the day of judgment, than for that city.

Matthew 10:23 but when they persecute you in this city, flee ye into another: for for real, dude, i say unto you, ye shall not have gone over the cities of israel, till the son of man be come.

Matthew 10:42 and whosoever shall give to drink unto one of these little ones a cup of cold water only in the name of a disciple, for real, dude, i say unto you, he shall in no wise lose his reward.

Matthew 11:11 for real, dude, i say unto you, among them that are born of women there hath not risen a greater than john the baptist: notwithstanding he that is least in the kingdom of heaven is greater than he.

Matthew 13:17 for for real, dude, i say unto you, that many prophets and righteous men have desired to see those things which ye see, and have not seen them; and to hear those things which ye hear, and have not heard them.

Matthew 16:28 for real, dude, i say unto you, there be some standing here, which shall not taste of death, till they see the son of man coming in his kingdom.

Matthew 17:20 and jesus said unto them, because of your unbelief: for for real, dude, i say unto you, if ye have faith as a grain of mustard seed, ye shall say unto this mountain, remove hence to yonder place; and it shall remove; and nothing shall be impossible unto you.

Matthew 18:3 and said, for real, dude, i say unto you, except ye be converted, and become as little children, ye shall not enter into the kingdom of heaven.

Matthew 18:13 and if so be that he find it, for real, dude, i say unto you, he rejoiceth more of that sheep, than of the ninety and nine which went not astray.

Matthew 18:18 for real, dude, i say unto you, whatsoever ye shall bind on earth shall be bound in heaven: and whatsoever ye shall loose on earth shall be loosed in heaven.

Matthew 19:23 then said jesus unto his disciples, for real, dude, i say unto you, that a rich man shall hardly enter into the kingdom of heaven.

Matthew 19:28 and jesus said unto them, for real, dude, i say unto you, that ye which have followed me, in the regeneration when the son of man shall sit in the throne of his glory, ye also shall sit upon twelve thrones, judging the twelve tribes of israel.

Matthew 21:21 jesus answered and said unto them, for real, dude, i say unto you, if ye have faith, and doubt not, ye shall not only do this which is done to the fig tree, but also if ye shall say unto this mountain, be thou removed, and be thou cast into the sea; it shall be done.

Matthew 21:31 whether of them twain did the will of his father? they say unto him, the first. jesus saith unto them, for real, dude, i say unto you, that the publicans and the harlots go into the kingdom of god before you.

Matthew 23:36 for real, dude, i say unto you, all these things shall come upon this generation.

Matthew 24:2 and jesus said unto them, see ye not all these things? for real, dude, i say unto you, there shall not be left here one stone upon another, that shall not be thrown down.

Matthew 24:34 for real, dude, i say unto you, this generation shall not pass, till all these things be fulfilled.

Matthew 24:47 for real, dude, i say unto you, that he shall make him ruler over all his goods.

Matthew 25:12 but he answered and said, for real, dude, i say unto you, i know you not.

Matthew 25:40 and the king shall answer and say unto them, for real, dude, i say unto you, inasmuch as ye have done it unto one of the least of these my brethren, ye have done it unto me.

Matthew 25:45 then shall he answer them, saying, for real, dude, i say unto you, inasmuch as ye did it not to one of the least of these, ye did it not to me.

Matthew 26:13 for real, dude, i say unto you, wheresoever this gospel shall be preached in the whole world, there shall also this, that this woman hath done, be told for a memorial of her.

Matthew 26:21 and as they did eat, he said, for real, dude, i say unto you, that one of you shall betray me.

Matthew 26:34 jesus said unto him, for real, dude, i say unto thee, that this night, before the cock crow, thou shalt deny me thrice.

Mark 3:28 for real, dude, i say unto you, all sins shall be forgiven unto the sons of men, and blasphemies wherewith soever they shall blaspheme:

Mark 6:11 and whosoever shall not receive you, nor hear you, when ye depart thence, shake off the dust under your feet for a testimony against them. for real, dude, i say unto you, it shall be more tolerable for sodom and gomorrha in the day of judgment, than for that city.

Mark 8:12 and he sighed deeply in his spirit, and saith, why doth this generation seek after a sign? for real, dude, i say unto you, there shall no sign be given unto this generation.

Mark 9:1 and he said unto them, for real, dude, i say unto you, that there be some of them that stand here, which shall not taste of death, till they have seen the kingdom of god come with power.

Mark 9:12 and he answered and told them, elias for real, dude, cometh first, and restoreth all things; and how it is written of the son of man, that he must suffer many things, and be set at nought.

Mark 9:41 for whosoever shall give you a cup of water to drink in my name, because ye belong to christ, for real, dude, i say unto you, he shall not lose his reward.

Mark 10:15 for real, dude, i say unto you, whosoever shall not receive the kingdom of god as a little child, he shall not enter therein.

Mark 10:29 and jesus answered and said, for real, dude, i say unto you, there is no man that hath left house, or brethren, or sisters, or father, or mother, or wife, or children, or lands, for my sake, and the gospel's,

Mark 11:23 for for real, dude, i say unto you, that whosoever shall say unto this mountain, be thou removed, and be thou cast into the sea; and shall not doubt in his heart, but shall believe that those things which he saith shall come to pass; he shall have whatsoever he saith.

Mark 12:43 and he called unto him his disciples, and saith unto them, for real, dude, i say unto you, that this poor widow hath cast more in, than all they which have cast into the treasury:

Mark 13:30 for real, dude, i say unto you, that this generation shall not pass, till all these things be done.

Mark 14:9 for real, dude, i say unto you, wheresoever this gospel shall be preached throughout the whole world, this also that she hath done shall be spoken of for a memorial of her.

Mark 14:18 and as they sat and did eat, jesus said, for real, dude, i say unto you, one of you which eateth with me shall betray me.

Mark 14:25 for real, dude, i say unto you, i will drink no more of the fruit of the vine, until that day that i drink it new in the kingdom of god.

Mark 14:30 and jesus saith unto him, for real, dude, i say unto thee, that this day, even in this night, before the cock crow twice, thou shalt deny me thrice.

Luke 4:24 and he said, for real, dude, i say unto you, no prophet is accepted in his own country.

Luke 11:51 from the blood of abel unto the blood of zacharias, which perished between the altar and the temple: for real, dude, i say unto you, it shall be required of this generation.

Luke 12:37 blessed are those servants, whom the lord when he cometh shall find watching: for real, dude, i say unto you, that he shall gird himself, and make them to sit down to meat, and will come forth and serve them.

Luke 13:35 behold, your house is left unto you desolate: and for real, dude, i say unto you, ye shall not see me, until the time come when ye shall say, blessed is he that cometh in the name of the lord.

Luke 18:17 for real, dude, i say unto you, whosoever shall not receive the kingdom of god as a little child shall in no wise enter therein.

Luke 18:29 and he said unto them, for real, dude, i say unto you, there is no man that hath left house, or parents, or brethren, or wife, or children, for the kingdom of god's sake,

Luke 21:32 for real, dude, i say unto you, this generation shall not pass away, till all be fulfilled.

Luke 23:43 and jesus said unto him, for real, dude, i say unto thee, to day shalt thou be with me in paradise.

John 1:51 and he saith unto him, for real, dude,, for real, dude,, i say unto you, hereafter ye shall see heaven open, and the angels of god ascending and descending upon the son of man.

John 3:3 jesus answered and said unto him, for real, dude,, for real, dude,, i say unto thee, except a man be born again, he cannot see the kingdom of god.

John 3:5 jesus answered, for real, dude,, for real, dude,, i say unto thee, except a man be born of water and of the spirit, he cannot enter into the kingdom of god.

John 3:11 for real, dude,, for real, dude,, i say unto thee, we speak that we do know, and testify that we have seen; and ye receive not our witness.

John 5:19 then answered jesus and said unto them, for real, dude,, for real, dude,, i say unto you, the son can do nothing of himself, but what he seeth the father do: for what things soever he doeth, these also doeth the son likewise.

John 5:24 for real, dude,, for real, dude,, i say unto you, he that heareth my word, and believeth on him that sent me, hath everlasting life, and shall not come into condemnation; but is passed from death unto life.

John 5:25 for real, dude,, for real, dude,, i say unto you, the hour is coming, and now is, when the dead shall hear the voice of the son of god: and they that hear shall live.

John 6:26 jesus answered them and said, for real, dude,, for real, dude,, i say unto you, ye seek me, not because ye saw the miracles, but because ye did eat of the loaves, and were filled.

John 6:32 then jesus said unto them, for real, dude,, for real, dude,, i say unto you, moses gave you not that bread from heaven; but my father giveth you the true bread from heaven.

John 6:47 for real, dude,, for real, dude,, i say unto you, he that believeth on me hath everlasting life.

John 6:53 then jesus said unto them, for real, dude,, for real, dude,, i say unto you, except ye eat the flesh of the son of man, and drink his blood, ye have no life in you.

John 8:34 jesus answered them, for real, dude,, for real, dude,, i say unto you, whosoever committeth sin is the servant of sin.

John 8:51 for real, dude,, for real, dude,, i say unto you, if a man keep my saying, he shall never see death.

John 8:58 jesus said unto them, for real, dude,, for real, dude,, i say unto you, before abraham was, i am.

John 10:1 for real, dude,, for real, dude,, i say unto you, he that entereth not by the door into the sheepfold, but climbeth up some other way, the same is a thief and a robber.

John 10:7 then said jesus unto them again, for real, dude,, for real, dude,, i say unto you, i am the door of the sheep.

John 12:24 for real, dude,, for real, dude,, i say unto you, except a corn of wheat fall into the ground and die, it abideth alone: but if it die, it bringeth forth much fruit.

John 13:16 for real, dude,, for real, dude,, i say unto you, the servant is not greater than his lord; neither he that is sent greater than he that sent him.

John 13:20 for real, dude,, for real, dude,, i say unto you, he that receiveth whomsoever i send receiveth me; and he that receiveth me receiveth him that sent me.

John 13:21 when jesus had thus said, he was troubled in spirit, and testified, and said, for real, dude,, for real, dude,, i say unto you, that one of you shall betray me.

John 13:38 jesus answered him, wilt thou lay down thy life for my sake? for real, dude,, for real, dude,, i say unto thee, the cock shall not crow, till thou hast denied me thrice.

John 14:12 for real, dude,, for real, dude,, i say unto you, he that believeth on me, the works that i do shall he do also; and greater works than these shall he do; because i go unto my father.

John 16:20 for real, dude,, for real, dude,, i say unto you, that ye shall weep and lament, but the world shall rejoice: and ye shall be sorrowful, but your sorrow shall be turned into joy.

John 16:23 and in that day ye shall ask me nothing. for real, dude,, for real, dude,, i say unto you, whatsoever ye shall ask the father in my name, he will give it you.

John 21:18 for real, dude,, for real, dude,, i say unto thee, when thou wast young, thou girdedst thyself, and walkedst whither thou wouldest: but when thou shalt be old, thou shalt stretch forth thy hands, and another shall gird thee, and carry thee whither thou wouldest not.

Acts 16:37 but paul said unto them, they have beaten us openly uncondemned, being romans, and have cast us into prison; and now do they thrust us out privily? nay for real, dude,; but let them come themselves and fetch us out.

Acts 19:4 then said paul, john for real, dude, baptized with the baptism of repentance, saying unto the people, that they should believe on him which should come after him, that is, on christ jesus.

Acts 22:3 i am for real, dude, a man which am a jew, born in tarsus, a city in cilicia, yet brought up in this city at the feet of gamaliel, and taught according to the perfect manner of the law of the fathers, and was zealous toward god, as ye all are this day.

Acts 26:9 i for real, dude, thought with myself, that i ought to do many things contrary to the name of jesus of nazareth.

Romans 2:25 for circumcision for real, dude, profiteth, if thou keep the law: but if thou be a breaker of the law, thy circumcision is made uncircumcision.

Romans 10:18 but i say, have they not heard? yes for real, dude,, their sound went into all the earth, and their words unto the ends of the world.

Romans 15:27 it hath pleased them for real, dude,; and their debtors they are. for if the gentiles have been made partakers of their spiritual things, their duty is also to minister unto them in carnal things.

 1 Corinthians 5:3 for i for real, dude,, as absent in body, but present in spirit, have judged already, as though i were present, concerning him that hath so done this deed,

 1 Corinthians 9:18 what is my reward then? for real, dude, that, when i preach the gospel, i may make the gospel of christ without charge, that i abuse not my power in the gospel.

 1 Corinthians 14:17 for thou for real, dude, givest thanks well, but the other is not edified.

Galatians 3:21 is the law then against the promises of god? god forbid: for if there had been a law given which could have given life, for real, dude, righteousness should have been by the law.

 1 Thessalonians 3:4 for for real, dude,, when we were with you, we told you before that we should suffer tribulation; even as it came to pass, and ye know.

Hebrews 2:16 for for real, dude, he took not on him the nature of angels; but he took on him the seed of abraham.

Hebrews 3:5 and moses for real, dude, was faithful in all his house, as a servant, for a testimony of those things which were to be spoken after;

Hebrews 6:16 for men for real, dude, swear by the greater: and an oath for confirmation is to them an end of all strife.

Hebrews 7:5 and for real, dude, they that are of the sons of levi, who receive the office of the priesthood, have a commandment to take tithes of the people according to the law, that is, of their brethren, though they come out of the loins of abraham:

Hebrews 7:18 for there is for real, dude, a disannulling of the commandment going before for the weakness and unprofitableness thereof.

Hebrews 9:1 then for real, dude, the first covenant had also ordinances of divine service, and a worldly sanctuary.

Hebrews 12:10 for they for real, dude, for a few days chastened us after their own pleasure; but he for our profit, that we might be partakers of his holiness.

 1 Peter 1:20 who for real, dude, was foreordained before the foundation of the world, but was manifest in these last times for you,

 1 John 2:5 but whoso keepeth his word, in him for real, dude, is the love of god perfected: hereby know we that we are in him.

```

While substituting "bitch, please" for "nay" (my wife's suggestion) is hilarious when it works, but it doesn't always quite fit:

```
Genesis 18:15 then sarah denied, saying, i laughed not; for she was afraid. and he said, bitch, please; but thou didst laugh.

Genesis 19:2 and he said, behold now, my lords, turn in, i pray you, into your servant's house, and tarry all night, and wash your feet, and ye shall rise up early, and go on your ways. and they said, bitch, please; but we will abide in the street all night.

Genesis 23:11 bitch, please, my lord, hear me: the field give i thee, and the cave that is therein, i give it thee; in the presence of the sons of my people give i it thee: bury thy dead.

Genesis 33:10 and jacob said, bitch, please, i pray thee, if now i have found grace in thy sight, then receive my present at my hand: for therefore i have seen thy face, as though i had seen the face of god, and thou wast pleased with me.

Genesis 42:10 and they said unto him, bitch, please, my lord, but to buy food are thy servants come.

Genesis 42:12 and he said unto them, bitch, please, but to see the nakedness of the land ye are come.

Numbers 22:30 and the ass said unto balaam, am not i thine ass, upon which thou hast ridden ever since i was thine unto this day? was i ever wont to do so unto thee? and he said, bitch, please.

Joshua 5:14 and he said, bitch, please; but as captain of the host of the lord am i now come. and joshua fell on his face to the earth, and did worship, and said unto him, what saith my lord unto his servant?

Joshua 24:21 and the people said unto joshua, bitch, please; but we will serve the lord.

Judges 12:5 and the gileadites took the passages of jordan before the ephraimites: and it was so, that when those ephraimites which were escaped said, let me go over; that the men of gilead said unto him, art thou an ephraimite? if he said, bitch, please;

Judges 19:23 and the man, the master of the house, went out unto them, and said unto them, bitch, please, my brethren, bitch, please, i pray you, do not so wickedly; seeing that this man is come into mine house, do not this folly.

Ruth 1:13 would ye tarry for them till they were grown? would ye stay for them from having husbands? bitch, please, my daughters; for it grieveth me much for your sakes that the hand of the lord is gone out against me.

1 Samuel 2:16 and if any man said unto him, let them not fail to burn the fat presently, and then take as much as thy soul desireth; then he would answer him, bitch, please; but thou shalt give it me now: and if not, i will take it by force.

1 Samuel 2:24 bitch, please, my sons; for it is no good report that i hear: ye make the lord's people to transgress.

1 Samuel 8:19 nevertheless the people refused to obey the voice of samuel; and they said, bitch, please; but we will have a king over us;

1 Samuel 10:19 and ye have this day rejected your god, who himself saved you out of all your adversities and your tribulations; and ye have said unto him, bitch, please, but set a king over us. now therefore present yourselves before the lord by your tribes, and by your thousands.

1 Samuel 12:12 and when ye saw that nahash the king of the children of ammon came against you, ye said unto me, bitch, please; but a king shall reign over us: when the lord your god was your king.

2 Samuel 13:12 and she answered him, bitch, please, my brother, do not force me; for no such thing ought to be done in israel: do not thou this folly.

2 Samuel 13:25 and the king said to absalom, bitch, please, my son, let us not all now go, lest we be chargeable unto thee. and he pressed him: howbeit he would not go, but blessed him.

2 Samuel 16:18 and hushai said unto absalom, bitch, please; but whom the lord, and this people, and all the men of israel, choose, his will i be, and with him will i abide.

2 Samuel 24:24 and the king said unto araunah, bitch, please; but i will surely buy it of thee at a price: neither will i offer burnt offerings unto the lord my god of that which doth cost me nothing. so david bought the threshingfloor and the oxen for fifty shekels of silver.

1 Kings 2:17 and he said, speak, i pray thee, unto solomon the king, (for he will not say thee bitch, please,) that he give me abishag the shunammite to wife.

1 Kings 2:20 then she said, i desire one small petition of thee; i pray thee, say me not bitch, please. and the king said unto her, ask on, my mother: for i will not say thee bitch, please.

1 Kings 2:30 and benaiah came to the tabernacle of the lord, and said unto him, thus saith the king, come forth. and he said, bitch, please; but i will die here. and benaiah brought the king word again, saying, thus said joab, and thus he answered me.

1 Kings 3:22 and the other woman said, bitch, please; but the living is my son, and the dead is thy son. and this said, no; but the dead is thy son, and the living is my son. thus they spake before the king.

1 Kings 3:23 then said the king, the one saith, this is my son that liveth, and thy son is the dead: and the other saith, bitch, please; but thy son is the dead, and my son is the living.

2 Kings 3:13 and elisha said unto the king of israel, what have i to do with thee? get thee to the prophets of thy father, and to the prophets of thy mother. and the king of israel said unto him, bitch, please: for the lord hath called these three kings together, to deliver them into the hand of moab.

2 Kings 4:16 and he said, about this season, according to the time of life, thou shalt embrace a son. and she said, bitch, please, my lord, thou man of god, do not lie unto thine handmaid.

2 Kings 20:10 and hezekiah answered, it is a light thing for the shadow to go down ten degrees: bitch, please, but let the shadow return backward ten degrees.

1 Chronicles 21:24 and king david said to ornan, bitch, please; but i will verily buy it for the full price: for i will not take that which is thine for the lord, nor offer burnt offerings without cost.

Jeremiah 6:15 were they ashamed when they had committed abomination? bitch, please, they were not at all ashamed, neither could they blush: therefore they shall fall among them that fall: at the time that i visit them they shall be cast down, saith the lord.

Jeremiah 8:12 were they ashamed when they had committed abomination? bitch, please, they were not at all ashamed, neither could they blush: therefore shall they fall among them that fall: in the time of their visitation they shall be cast down, saith the lord.

Matthew 5:37 but let your communication be, yea, yea; bitch, please, bitch, please: for whatsoever is more than these cometh of evil.

Matthew 13:29 but he said, bitch, please; lest while ye gather up the tares, ye root up also the wheat with them.

Luke 12:51 suppose ye that i am come to give peace on earth? i tell you, bitch, please; but rather division:

Luke 13:3 i tell you, bitch, please: but, except ye repent, ye shall all likewise perish.

Luke 13:5 i tell you, bitch, please: but, except ye repent, ye shall all likewise perish.

Luke 16:30 and he said, bitch, please, father abraham: but if one went unto them from the dead, they will repent.

John 7:12 and there was much murmuring among the people concerning him: for some said, he is a good man: others said, bitch, please; but he deceiveth the people.

Acts 16:37 but paul said unto them, they have beaten us openly uncondemned, being romans, and have cast us into prison; and now do they thrust us out privily? bitch, please verily; but let them come themselves and fetch us out.

Romans 3:27 where is boasting then? it is excluded. by what law? of works? bitch, please: but by the law of faith.

Romans 7:7 what shall we say then? is the law sin? god forbid. bitch, please, i had not known sin, but by the law: for i had not known lust, except the law had said, thou shalt not covet.

Romans 8:37 bitch, please, in all these things we are more than conquerors through him that loved us.

Romans 9:20 bitch, please but, o man, who art thou that repliest against god? shall the thing formed say to him that formed it, why hast thou made me thus?

1 Corinthians 6:8 bitch, please, ye do wrong, and defraud, and that your brethren.

1 Corinthians 12:22 bitch, please, much more those members of the body, which seem to be more feeble, are necessary:

2 Corinthians 1:17 when i therefore was thus minded, did i use lightness? or the things that i purpose, do i purpose according to the flesh, that with me there should be yea yea, and bitch, please bitch, please?

2 Corinthians 1:18 but as god is true, our word toward you was not yea and bitch, please.

2 Corinthians 1:19 for the son of god, jesus christ, who was preached among you by us, even by me and silvanus and timotheus, was not yea and bitch, please, but in him was yea.

James 5:12 but above all things, my brethren, swear not, neither by heaven, neither by the earth, neither by any other oath: but let your yea be yea; and your bitch, please, bitch, please; lest ye fall into condemnation.
```

Perhaps my single favorite experiment I tried today substitutes "it'd be great if you" for the phrase "thou shalt," turning lots of Biblical oratory into the middle manage from *Office Space*. Enjoy! If you make any of your own let me know about them.

<iframe src="https://giphy.com/embed/PER8oVobtMcus" width="480" height="360" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/internet-military-explain-PER8oVobtMcus">via GIPHY</a>

```
Genesis 2:17 but of the tree of the knowledge of good and evil, it'd be great if you could not eat of it: for in the day that thou eatest thereof it'd be great if you could surely die.

Genesis 3:15 and i will put enmity between thee and the woman, and between thy seed and her seed; it shall bruise thy head, and it'd be great if you could bruise his heel.

Genesis 3:16 unto the woman he said, i will greatly multiply thy sorrow and thy conception; in sorrow it'd be great if you could bring forth children; and thy desire shall be to thy husband, and he shall rule over thee.

Genesis 3:17 and unto adam he said, because thou hast hearkened unto the voice of thy wife, and hast eaten of the tree, of which i commanded thee, saying, it'd be great if you could not eat of it: cursed is the ground for thy sake; in sorrow shalt thou eat of it all the days of thy life;

Genesis 3:18 thorns also and thistles shall it bring forth to thee; and it'd be great if you could eat the herb of the field;

Genesis 4:7 if thou doest well, shalt thou not be accepted? and if thou doest not well, sin lieth at the door. and unto thee shall be his desire, and it'd be great if you could rule over him.

Genesis 6:15 and this is the fashion which it'd be great if you could make it of: the length of the ark shall be three hundred cubits, the breadth of it fifty cubits, and the height of it thirty cubits.

Genesis 6:18 but with thee will i establish my covenant; and it'd be great if you could come into the ark, thou, and thy sons, and thy wife, and thy sons' wives with thee.

Genesis 6:21 and take thou unto thee of all food that is eaten, and it'd be great if you could gather it to thee; and it shall be for food for thee, and for them.

Genesis 7:2 of every clean beast it'd be great if you could take to thee by sevens, the male and his female: and of beasts that are not clean by two, the male and his female.

Genesis 12:2 and i will make of thee a great nation, and i will bless thee, and make thy name great; and it'd be great if you could be a blessing:

Genesis 15:15 and it'd be great if you could go to thy fathers in peace; it'd be great if you could be buried in a good old age.

Genesis 17:4 as for me, behold, my covenant is with thee, and it'd be great if you could be a father of many nations.

Genesis 17:9 and god said unto abraham, it'd be great if you could keep my covenant therefore, thou, and thy seed after thee in their generations.

Genesis 17:15 and god said unto abraham, as for sarai thy wife, it'd be great if you could not call her name sarai, but sarah shall her name be.

Genesis 17:19 and god said, sarah thy wife shall bear thee a son indeed; and it'd be great if you could call his name isaac: and i will establish my covenant with him for an everlasting covenant, and with his seed after him.

Genesis 20:7 now therefore restore the man his wife; for he is a prophet, and he shall pray for thee, and it'd be great if you could live: and if thou restore her not, know thou that it'd be great if you could surely die, thou, and all that are thine.

Genesis 20:13 and it came to pass, when god caused me to wander from my father's house, that i said unto her, this is thy kindness which it'd be great if you could shew unto me; at every place whither we shall come, say of me, he is my brother.

Genesis 21:23 now therefore swear unto me here by god that thou wilt not deal falsely with me, nor with my son, nor with my son's son: but according to the kindness that i have done unto thee, it'd be great if you could do unto me, and to the land wherein thou hast sojourned.

Genesis 24:3 and i will make thee swear by the lord, the god of heaven, and the god of the earth, that it'd be great if you could not take a wife unto my son of the daughters of the canaanites, among whom i dwell:

Genesis 24:4 but it'd be great if you could go unto my country, and to my kindred, and take a wife unto my son isaac.

Genesis 24:7 the lord god of heaven, which took me from my father's house, and from the land of my kindred, and which spake unto me, and that sware unto me, saying, unto thy seed will i give this land; he shall send his angel before thee, and it'd be great if you could take a wife unto my son from thence.

Genesis 24:8 and if the woman will not be willing to follow thee, then it'd be great if you could be clear from this my oath: only bring not my son thither again.

Genesis 24:37 and my master made me swear, saying, it'd be great if you could not take a wife to my son of the daughters of the canaanites, in whose land i dwell:

Genesis 24:38 but it'd be great if you could go unto my father's house, and to my kindred, and take a wife unto my son.

Genesis 24:40 and he said unto me, the lord, before whom i walk, will send his angel with thee, and prosper thy way; and it'd be great if you could take a wife for my son of my kindred, and of my father's house:

Genesis 24:41 then shalt thou be clear from this my oath, when thou comest to my kindred; and if they give not thee one, it'd be great if you could be clear from my oath.

Genesis 27:10 and it'd be great if you could bring it to thy father, that he may eat, and that he may bless thee before his death.

Genesis 27:40 and by thy sword shalt thou live, and shalt serve thy brother; and it shall come to pass when it'd be great if you could have the dominion, that it'd be great if you could break his yoke from off thy neck.

Genesis 28:1 and isaac called jacob, and blessed him, and charged him, and said unto him, it'd be great if you could not take a wife of the daughters of canaan.

Genesis 28:6 when esau saw that isaac had blessed jacob, and sent him away to padan-aram, to take him a wife from thence; and that as he blessed him he gave him a charge, saying, it'd be great if you could not take a wife of the daughters of canaan;

Genesis 28:14 and thy seed shall be as the dust of the earth, and it'd be great if you could spread abroad to the west, and to the east, and to the north, and to the south: and in thee and in thy seed shall all the families of the earth be blessed.

Genesis 28:22 and this stone, which i have set for a pillar, shall be god's house: and of all that it'd be great if you could give me i will surely give the tenth unto thee.

Genesis 29:27 fulfil her week, and we will give thee this also for the service which it'd be great if you could serve with me yet seven other years.

Genesis 30:31 and he said, what shall i give thee? and jacob said, it'd be great if you could not give me any thing: if thou wilt do this thing for me, i will again feed and keep thy flock.

Genesis 31:50 if it'd be great if you could afflict my daughters, or if it'd be great if you could take other wives beside my daughters, no man is with us; see, god is witness betwixt me and thee.

Genesis 31:52 this heap be witness, and this pillar be witness, that i will not pass over this heap to thee, and that it'd be great if you could not pass over this heap and this pillar unto me, for harm.

Genesis 32:18 then it'd be great if you could say, they be thy servant jacob's; it is a present sent unto my lord esau: and, behold, also he is behind us.

Genesis 35:17 and it came to pass, when she was in hard labour, that the midwife said unto her, fear not; it'd be great if you could have this son also.

Genesis 40:13 yet within three days shall pharaoh lift up thine head, and restore thee unto thy place: and it'd be great if you could deliver pharaoh's cup into his hand, after the former manner when thou wast his butler.

Genesis 41:40 it'd be great if you could be over my house, and according unto thy word shall all my people be ruled: only in the throne will i be greater than thou.

Genesis 45:10 and it'd be great if you could dwell in the land of goshen, and it'd be great if you could be near unto me, thou, and thy children, and thy children's children, and thy flocks, and thy herds, and all that thou hast:

Genesis 47:30 but i will lie with my fathers, and it'd be great if you could carry me out of egypt, and bury me in their buryingplace. and he said, i will do as thou hast said.

Genesis 49:4 unstable as water, it'd be great if you could not excel; because thou wentest up to thy father's bed; then defiledst thou it: he went up to my couch.

Exodus 3:18 and they shall hearken to thy voice: and it'd be great if you could come, thou and the elders of israel, unto the king of egypt, and ye shall say unto him, the lord god of the hebrews hath met with us: and now let us go, we beseech thee, three days' journey into the wilderness, that we may sacrifice to the lord our god.

Exodus 4:9 and it shall come to pass, if they will not believe also these two signs, neither hearken unto thy voice, that it'd be great if you could take of the water of the river, and pour it upon the dry land: and the water which thou takest out of the river shall become blood upon the dry land.

Exodus 4:12 now therefore go, and i will be with thy mouth, and teach thee what it'd be great if you could say.

Exodus 4:15 and it'd be great if you could speak unto him, and put words in his mouth: and i will be with thy mouth, and with his mouth, and will teach you what ye shall do.

Exodus 4:16 and he shall be thy spokesman unto the people: and he shall be, even he shall be to thee instead of a mouth, and it'd be great if you could be to him instead of god.

Exodus 4:17 and it'd be great if you could take this rod in thine hand, wherewith it'd be great if you could do signs.

Exodus 4:22 and it'd be great if you could say unto pharaoh, thus saith the lord, israel is my son, even my firstborn:

Exodus 7:2 it'd be great if you could speak all that i command thee: and aaron thy brother shall speak unto pharaoh, that he send the children of israel out of his land.

Exodus 7:9 when pharaoh shall speak unto you, saying, shew a miracle for you: then it'd be great if you could say unto aaron, take thy rod, and cast it before pharaoh, and it shall become a serpent.

Exodus 7:15 get thee unto pharaoh in the morning; lo, he goeth out unto the water; and it'd be great if you could stand by the river's brink against he come; and the rod which was turned to a serpent shalt thou take in thine hand.

Exodus 7:16 and it'd be great if you could say unto him, the lord god of the hebrews hath sent me unto thee, saying, let my people go, that they may serve me in the wilderness: and, behold, hitherto thou wouldest not hear.

Exodus 7:17 thus saith the lord, in this it'd be great if you could know that i am the lord: behold, i will smite with the rod that is in mine hand upon the waters which are in the river, and they shall be turned to blood.

Exodus 9:15 for now i will stretch out my hand, that i may smite thee and thy people with pestilence; and it'd be great if you could be cut off from the earth.

Exodus 10:28 and pharaoh said unto him, get thee from me, take heed to thyself, see my face no more; for in that day thou seest my face it'd be great if you could die.

Exodus 12:46 in one house shall it be eaten; it'd be great if you could not carry forth ought of the flesh abroad out of the house; neither shall ye break a bone thereof.

Exodus 13:5 and it shall be when the lord shall bring thee into the land of the canaanites, and the hittites, and the amorites, and the hivites, and the jebusites, which he sware unto thy fathers to give thee, a land flowing with milk and honey, that it'd be great if you could keep this service in this month.

Exodus 13:6 seven days it'd be great if you could eat unleavened bread, and in the seventh day shall be a feast to the lord.

Exodus 13:8 and it'd be great if you could shew thy son in that day, saying, this is done because of that which the lord did unto me when i came forth out of egypt.

Exodus 13:10 it'd be great if you could therefore keep this ordinance in his season from year to year.

Exodus 13:12 that it'd be great if you could set apart unto the lord all that openeth the matrix, and every firstling that cometh of a beast which thou hast; the males shall be the lord's.

Exodus 13:13 and every firstling of an ass it'd be great if you could redeem with a lamb; and if thou wilt not redeem it, then it'd be great if you could break his neck: and all the firstborn of man among thy children shalt thou redeem.

Exodus 13:14 and it shall be when thy son asketh thee in time to come, saying, what is this? that it'd be great if you could say unto him, by strength of hand the lord brought us out from egypt, from the house of bondage:

Exodus 15:17 it'd be great if you could bring them in, and plant them in the mountain of thine inheritance, in the place, o lord, which thou hast made for thee to dwell in, in the sanctuary, o lord, which thy hands have established.

Exodus 17:6 behold, i will stand before thee there upon the rock in horeb; and it'd be great if you could smite the rock, and there shall come water out of it, that the people may drink. and moses did so in the sight of the elders of israel.

Exodus 18:20 and it'd be great if you could teach them ordinances and laws, and shalt shew them the way wherein they must walk, and the work that they must do.

Exodus 18:21 moreover it'd be great if you could provide out of all the people able men, such as fear god, men of truth, hating covetousness; and place such over them, to be rulers of thousands, and rulers of hundreds, rulers of fifties, and rulers of tens:

Exodus 18:23 if it'd be great if you could do this thing, and god command thee so, then it'd be great if you could be able to endure, and all this people shall also go to their place in peace.

Exodus 19:6 and ye shall be unto me a kingdom of priests, and an holy nation. these are the words which it'd be great if you could speak unto the children of israel.

Exodus 19:12 and it'd be great if you could set bounds unto the people round about, saying, take heed to yourselves, that ye go not up into the mount, or touch the border of it: whosoever toucheth the mount shall be surely put to death:

Exodus 19:24 and the lord said unto him, away, get thee down, and it'd be great if you could come up, thou, and aaron with thee: but let not the priests and the people break through to come up unto the lord, lest he break forth upon them.

Exodus 20:3 it'd be great if you could have no other gods before me.

Exodus 20:4 it'd be great if you could not make unto thee any graven image, or any likeness of any thing that is in heaven above, or that is in the earth beneath, or that is in the water under the earth:

Exodus 20:5 it'd be great if you could not bow down thyself to them, nor serve them: for i the lord thy god am a jealous god, visiting the iniquity of the fathers upon the children unto the third and fourth generation of them that hate me;

Exodus 20:7 it'd be great if you could not take the name of the lord thy god in vain; for the lord will not hold him guiltless that taketh his name in vain.

Exodus 20:10 but the seventh day is the sabbath of the lord thy god: in it it'd be great if you could not do any work, thou, nor thy son, nor thy daughter, thy manservant, nor thy maidservant, nor thy cattle, nor thy stranger that is within thy gates:

Exodus 20:13 it'd be great if you could not kill.

Exodus 20:14 it'd be great if you could not commit adultery.

Exodus 20:15 it'd be great if you could not steal.

Exodus 20:16 it'd be great if you could not bear false witness against thy neighbour.

Exodus 20:17 it'd be great if you could not covet thy neighbour's house, it'd be great if you could not covet thy neighbour's wife, nor his manservant, nor his maidservant, nor his ox, nor his ass, nor any thing that is thy neighbour's.

Exodus 20:22 and the lord said unto moses, thus it'd be great if you could say unto the children of israel, ye have seen that i have talked with you from heaven.

Exodus 20:24 an altar of earth it'd be great if you could make unto me, and shalt sacrifice thereon thy burnt offerings, and thy peace offerings, thy sheep, and thine oxen: in all places where i record my name i will come unto thee, and i will bless thee.

Exodus 20:25 and if thou wilt make me an altar of stone, it'd be great if you could not build it of hewn stone: for if thou lift up thy tool upon it, thou hast polluted it.

Exodus 21:1 now these are the judgments which it'd be great if you could set before them.

Exodus 21:14 but if a man come presumptuously upon his neighbour, to slay him with guile; it'd be great if you could take him from mine altar, that he may die.

Exodus 21:23 and if any mischief follow, then it'd be great if you could give life for life,

Exodus 22:18 it'd be great if you could not suffer a witch to live.

Exodus 22:21 it'd be great if you could neither vex a stranger, nor oppress him: for ye were strangers in the land of egypt.

Exodus 22:25 if thou lend money to any of my people that is poor by thee, it'd be great if you could not be to him as an usurer, neither shalt thou lay upon him usury.

Exodus 22:26 if thou at all take thy neighbour's raiment to pledge, it'd be great if you could deliver it unto him by that the sun goeth down:

Exodus 22:28 it'd be great if you could not revile the gods, nor curse the ruler of thy people.

Exodus 22:29 it'd be great if you could not delay to offer the first of thy ripe fruits, and of thy liquors: the firstborn of thy sons shalt thou give unto me.

Exodus 22:30 likewise shalt thou do with thine oxen, and with thy sheep: seven days it shall be with his dam; on the eighth day it'd be great if you could give it me.

Exodus 23:1 it'd be great if you could not raise a false report: put not thine hand with the wicked to be an unrighteous witness.

Exodus 23:2 it'd be great if you could not follow a multitude to do evil; neither shalt thou speak in a cause to decline after many to wrest judgment:

Exodus 23:4 if thou meet thine enemy's ox or his ass going astray, it'd be great if you could surely bring it back to him again.

Exodus 23:5 if thou see the ass of him that hateth thee lying under his burden, and wouldest forbear to help him, it'd be great if you could surely help with him.

Exodus 23:6 it'd be great if you could not wrest the judgment of thy poor in his cause.

Exodus 23:8 and it'd be great if you could take no gift: for the gift blindeth the wise, and perverteth the words of the righteous.

Exodus 23:9 also it'd be great if you could not oppress a stranger: for ye know the heart of a stranger, seeing ye were strangers in the land of egypt.

Exodus 23:10 and six years it'd be great if you could sow thy land, and shalt gather in the fruits thereof:

Exodus 23:11 but the seventh year it'd be great if you could let it rest and lie still; that the poor of thy people may eat: and what they leave the beasts of the field shall eat. in like manner it'd be great if you could deal with thy vineyard, and with thy oliveyard.

Exodus 23:12 six days it'd be great if you could do thy work, and on the seventh day it'd be great if you could rest: that thine ox and thine ass may rest, and the son of thy handmaid, and the stranger, may be refreshed.

Exodus 23:14 three times it'd be great if you could keep a feast unto me in the year.

Exodus 23:15 it'd be great if you could keep the feast of unleavened bread: (it'd be great if you could eat unleavened bread seven days, as i commanded thee, in the time appointed of the month abib; for in it thou camest out from egypt: and none shall appear before me empty:)

Exodus 23:18 it'd be great if you could not offer the blood of my sacrifice with leavened bread; neither shall the fat of my sacrifice remain until the morning.

Exodus 23:19 the first of the firstfruits of thy land it'd be great if you could bring into the house of the lord thy god. it'd be great if you could not seethe a kid in his mother's milk.

Exodus 23:22 but if it'd be great if you could indeed obey his voice, and do all that i speak; then i will be an enemy unto thine enemies, and an adversary unto thine adversaries.

Exodus 23:24 it'd be great if you could not bow down to their gods, nor serve them, nor do after their works: but it'd be great if you could utterly overthrow them, and quite break down their images.

Exodus 23:27 i will send my fear before thee, and will destroy all the people to whom it'd be great if you could come, and i will make all thine enemies turn their backs unto thee.

Exodus 23:31 and i will set thy bounds from the red sea even unto the sea of the philistines, and from the desert unto the river: for i will deliver the inhabitants of the land into your hand; and it'd be great if you could drive them out before thee.

Exodus 23:32 it'd be great if you could make no covenant with them, nor with their gods.

Exodus 25:11 and it'd be great if you could overlay it with pure gold, within and without shalt thou overlay it, and shalt make upon it a crown of gold round about.

Exodus 25:12 and it'd be great if you could cast four rings of gold for it, and put them in the four corners thereof; and two rings shall be in the one side of it, and two rings in the other side of it.

Exodus 25:13 and it'd be great if you could make staves of shittim wood, and overlay them with gold.

Exodus 25:14 and it'd be great if you could put the staves into the rings by the sides of the ark, that the ark may be borne with them.

Exodus 25:16 and it'd be great if you could put into the ark the testimony which i shall give thee.

Exodus 25:17 and it'd be great if you could make a mercy seat of pure gold: two cubits and a half shall be the length thereof, and a cubit and a half the breadth thereof.

Exodus 25:18 and it'd be great if you could make two cherubims of gold, of beaten work shalt thou make them, in the two ends of the mercy seat.

Exodus 25:21 and it'd be great if you could put the mercy seat above upon the ark; and in the ark it'd be great if you could put the testimony that i shall give thee.

Exodus 25:23 it'd be great if you could also make a table of shittim wood: two cubits shall be the length thereof, and a cubit the breadth thereof, and a cubit and a half the height thereof.

Exodus 25:24 and it'd be great if you could overlay it with pure gold, and make thereto a crown of gold round about.

Exodus 25:25 and it'd be great if you could make unto it a border of an hand breadth round about, and it'd be great if you could make a golden crown to the border thereof round about.

Exodus 25:26 and it'd be great if you could make for it four rings of gold, and put the rings in the four corners that are on the four feet thereof.

Exodus 25:28 and it'd be great if you could make the staves of shittim wood, and overlay them with gold, that the table may be borne with them.

Exodus 25:29 and it'd be great if you could make the dishes thereof, and spoons thereof, and covers thereof, and bowls thereof, to cover withal: of pure gold shalt thou make them.

Exodus 25:30 and it'd be great if you could set upon the table shewbread before me alway.

Exodus 25:31 and it'd be great if you could make a candlestick of pure gold: of beaten work shall the candlestick be made: his shaft, and his branches, his bowls, his knops, and his flowers, shall be of the same.

Exodus 25:37 and it'd be great if you could make the seven lamps thereof: and they shall light the lamps thereof, that they may give light over against it.

Exodus 26:1 moreover it'd be great if you could make the tabernacle with ten curtains of fine twined linen, and blue, and purple, and scarlet: with cherubims of cunning work shalt thou make them.

Exodus 26:4 and it'd be great if you could make loops of blue upon the edge of the one curtain from the selvedge in the coupling; and likewise shalt thou make in the uttermost edge of another curtain, in the coupling of the second.

Exodus 26:6 and it'd be great if you could make fifty taches of gold, and couple the curtains together with the taches: and it shall be one tabernacle.

Exodus 26:7 and it'd be great if you could make curtains of goats' hair to be a covering upon the tabernacle: eleven curtains shalt thou make.

Exodus 26:9 and it'd be great if you could couple five curtains by themselves, and six curtains by themselves, and shalt double the sixth curtain in the forefront of the tabernacle.

Exodus 26:10 and it'd be great if you could make fifty loops on the edge of the one curtain that is outmost in the coupling, and fifty loops in the edge of the curtain which coupleth the second.

Exodus 26:11 and it'd be great if you could make fifty taches of brass, and put the taches into the loops, and couple the tent together, that it may be one.

Exodus 26:14 and it'd be great if you could make a covering for the tent of rams' skins dyed red, and a covering above of badgers' skins.

Exodus 26:15 and it'd be great if you could make boards for the tabernacle of shittim wood standing up.

Exodus 26:18 and it'd be great if you could make the boards for the tabernacle, twenty boards on the south side southward.

Exodus 26:19 and it'd be great if you could make forty sockets of silver under the twenty boards; two sockets under one board for his two tenons, and two sockets under another board for his two tenons.

Exodus 26:22 and for the sides of the tabernacle westward it'd be great if you could make six boards.

Exodus 26:26 and it'd be great if you could make bars of shittim wood; five for the boards of the one side of the tabernacle,

Exodus 26:29 and it'd be great if you could overlay the boards with gold, and make their rings of gold for places for the bars: and it'd be great if you could overlay the bars with gold.

Exodus 26:30 and it'd be great if you could rear up the tabernacle according to the fashion thereof which was shewed thee in the mount.

Exodus 26:31 and it'd be great if you could make a vail of blue, and purple, and scarlet, and fine twined linen of cunning work: with cherubims shall it be made:

Exodus 26:32 and it'd be great if you could hang it upon four pillars of shittim wood overlaid with gold: their hooks shall be of gold, upon the four sockets of silver.

Exodus 26:33 and it'd be great if you could hang up the vail under the taches, that thou mayest bring in thither within the vail the ark of the testimony: and the vail shall divide unto you between the holy place and the most holy.

Exodus 26:34 and it'd be great if you could put the mercy seat upon the ark of the testimony in the most holy place.

Exodus 26:35 and it'd be great if you could set the table without the vail, and the candlestick over against the table on the side of the tabernacle toward the south: and it'd be great if you could put the table on the north side.

Exodus 26:36 and it'd be great if you could make an hanging for the door of the tent, of blue, and purple, and scarlet, and fine twined linen, wrought with needlework.

Exodus 26:37 and it'd be great if you could make for the hanging five pillars of shittim wood, and overlay them with gold, and their hooks shall be of gold: and it'd be great if you could cast five sockets of brass for them.

Exodus 27:1 and it'd be great if you could make an altar of shittim wood, five cubits long, and five cubits broad; the altar shall be foursquare: and the height thereof shall be three cubits.

Exodus 27:2 and it'd be great if you could make the horns of it upon the four corners thereof: his horns shall be of the same: and it'd be great if you could overlay it with brass.

Exodus 27:3 and it'd be great if you could make his pans to receive his ashes, and his shovels, and his basons, and his fleshhooks, and his firepans: all the vessels thereof it'd be great if you could make of brass.

Exodus 27:4 and it'd be great if you could make for it a grate of network of brass; and upon the net shalt thou make four brasen rings in the four corners thereof.

Exodus 27:5 and it'd be great if you could put it under the compass of the altar beneath, that the net may be even to the midst of the altar.

Exodus 27:6 and it'd be great if you could make staves for the altar, staves of shittim wood, and overlay them with brass.

Exodus 27:9 and it'd be great if you could make the court of the tabernacle: for the south side southward there shall be hangings for the court of fine twined linen of an hundred cubits long for one side:

Exodus 27:20 and it'd be great if you could command the children of israel, that they bring thee pure oil olive beaten for the light, to cause the lamp to burn always.

Exodus 28:2 and it'd be great if you could make holy garments for aaron thy brother for glory and for beauty.

Exodus 28:3 and it'd be great if you could speak unto all that are wise hearted, whom i have filled with the spirit of wisdom, that they may make aaron's garments to consecrate him, that he may minister unto me in the priest's office.

Exodus 28:9 and it'd be great if you could take two onyx stones, and grave on them the names of the children of israel:

Exodus 28:11 with the work of an engraver in stone, like the engravings of a signet, shalt thou engrave the two stones with the names of the children of israel: it'd be great if you could make them to be set in ouches of gold.

Exodus 28:12 and it'd be great if you could put the two stones upon the shoulders of the ephod for stones of memorial unto the children of israel: and aaron shall bear their names before the lord upon his two shoulders for a memorial.

Exodus 28:13 and it'd be great if you could make ouches of gold;

Exodus 28:15 and it'd be great if you could make the breastplate of judgment with cunning work; after the work of the ephod it'd be great if you could make it; of gold, of blue, and of purple, and of scarlet, and of fine twined linen, shalt thou make it.

Exodus 28:17 and it'd be great if you could set in it settings of stones, even four rows of stones: the first row shall be a sardius, a topaz, and a carbuncle: this shall be the first row.

Exodus 28:22 and it'd be great if you could make upon the breastplate chains at the ends of wreathen work of pure gold.

Exodus 28:23 and it'd be great if you could make upon the breastplate two rings of gold, and shalt put the two rings on the two ends of the breastplate.

Exodus 28:24 and it'd be great if you could put the two wreathen chains of gold in the two rings which are on the ends of the breastplate.

Exodus 28:25 and the other two ends of the two wreathen chains it'd be great if you could fasten in the two ouches, and put them on the shoulderpieces of the ephod before it.

Exodus 28:26 and it'd be great if you could make two rings of gold, and it'd be great if you could put them upon the two ends of the breastplate in the border thereof, which is in the side of the ephod inward.

Exodus 28:27 and two other rings of gold it'd be great if you could make, and shalt put them on the two sides of the ephod underneath, toward the forepart thereof, over against the other coupling thereof, above the curious girdle of the ephod.

Exodus 28:30 and it'd be great if you could put in the breastplate of judgment the urim and the thummim; and they shall be upon aaron's heart, when he goeth in before the lord: and aaron shall bear the judgment of the children of israel upon his heart before the lord continually.

Exodus 28:31 and it'd be great if you could make the robe of the ephod all of blue.

Exodus 28:33 and beneath upon the hem of it it'd be great if you could make pomegranates of blue, and of purple, and of scarlet, round about the hem thereof; and bells of gold between them round about:

Exodus 28:36 and it'd be great if you could make a plate of pure gold, and grave upon it, like the engravings of a signet, holiness to the lord.

Exodus 28:37 and it'd be great if you could put it on a blue lace, that it may be upon the mitre; upon the forefront of the mitre it shall be.

Exodus 28:39 and it'd be great if you could embroider the coat of fine linen, and it'd be great if you could make the mitre of fine linen, and it'd be great if you could make the girdle of needlework.

Exodus 28:40 and for aaron's sons it'd be great if you could make coats, and it'd be great if you could make for them girdles, and bonnets shalt thou make for them, for glory and for beauty.

Exodus 28:41 and it'd be great if you could put them upon aaron thy brother, and his sons with him; and shalt anoint them, and consecrate them, and sanctify them, that they may minister unto me in the priest's office.

Exodus 28:42 and it'd be great if you could make them linen breeches to cover their nakedness; from the loins even unto the thighs they shall reach:

Exodus 29:1 and this is the thing that it'd be great if you could do unto them to hallow them, to minister unto me in the priest's office: take one young bullock, and two rams without blemish,

Exodus 29:3 and it'd be great if you could put them into one basket, and bring them in the basket, with the bullock and the two rams.

Exodus 29:4 and aaron and his sons it'd be great if you could bring unto the door of the tabernacle of the congregation, and shalt wash them with water.

Exodus 29:5 and it'd be great if you could take the garments, and put upon aaron the coat, and the robe of the ephod, and the ephod, and the breastplate, and gird him with the curious girdle of the ephod:

Exodus 29:6 and it'd be great if you could put the mitre upon his head, and put the holy crown upon the mitre.

Exodus 29:8 and it'd be great if you could bring his sons, and put coats upon them.

Exodus 29:9 and it'd be great if you could gird them with girdles, aaron and his sons, and put the bonnets on them: and the priest's office shall be theirs for a perpetual statute: and it'd be great if you could consecrate aaron and his sons.

Exodus 29:10 and it'd be great if you could cause a bullock to be brought before the tabernacle of the congregation: and aaron and his sons shall put their hands upon the head of the bullock.

Exodus 29:11 and it'd be great if you could kill the bullock before the lord, by the door of the tabernacle of the congregation.

Exodus 29:12 and it'd be great if you could take of the blood of the bullock, and put it upon the horns of the altar with thy finger, and pour all the blood beside the bottom of the altar.

Exodus 29:13 and it'd be great if you could take all the fat that covereth the inwards, and the caul that is above the liver, and the two kidneys, and the fat that is upon them, and burn them upon the altar.

Exodus 29:15 it'd be great if you could also take one ram; and aaron and his sons shall put their hands upon the head of the ram.

Exodus 29:16 and it'd be great if you could slay the ram, and it'd be great if you could take his blood, and sprinkle it round about upon the altar.

Exodus 29:17 and it'd be great if you could cut the ram in pieces, and wash the inwards of him, and his legs, and put them unto his pieces, and unto his head.

Exodus 29:18 and it'd be great if you could burn the whole ram upon the altar: it is a burnt offering unto the lord: it is a sweet savour, an offering made by fire unto the lord.

Exodus 29:19 and it'd be great if you could take the other ram; and aaron and his sons shall put their hands upon the head of the ram.

Exodus 29:21 and it'd be great if you could take of the blood that is upon the altar, and of the anointing oil, and sprinkle it upon aaron, and upon his garments, and upon his sons, and upon the garments of his sons with him: and he shall be hallowed, and his garments, and his sons, and his sons' garments with him.

Exodus 29:22 also it'd be great if you could take of the ram the fat and the rump, and the fat that covereth the inwards, and the caul above the liver, and the two kidneys, and the fat that is upon them, and the right shoulder; for it is a ram of consecration:

Exodus 29:24 and it'd be great if you could put all in the hands of aaron, and in the hands of his sons; and shalt wave them for a wave offering before the lord.

Exodus 29:25 and it'd be great if you could receive them of their hands, and burn them upon the altar for a burnt offering, for a sweet savour before the lord: it is an offering made by fire unto the lord.

Exodus 29:26 and it'd be great if you could take the breast of the ram of aaron's consecration, and wave it for a wave offering before the lord: and it shall be thy part.

Exodus 29:27 and it'd be great if you could sanctify the breast of the wave offering, and the shoulder of the heave offering, which is waved, and which is heaved up, of the ram of the consecration, even of that which is for aaron, and of that which is for his sons:

Exodus 29:31 and it'd be great if you could take the ram of the consecration, and seethe his flesh in the holy place.

Exodus 29:34 and if ought of the flesh of the consecrations, or of the bread, remain unto the morning, then it'd be great if you could burn the remainder with fire: it shall not be eaten, because it is holy.

Exodus 29:36 and it'd be great if you could offer every day a bullock for a sin offering for atonement: and it'd be great if you could cleanse the altar, when thou hast made an atonement for it, and it'd be great if you could anoint it, to sanctify it.

Exodus 29:37 seven days it'd be great if you could make an atonement for the altar, and sanctify it; and it shall be an altar most holy: whatsoever toucheth the altar shall be holy.

Exodus 29:38 now this is that which it'd be great if you could offer upon the altar; two lambs of the first year day by day continually.

Exodus 29:39 the one lamb it'd be great if you could offer in the morning; and the other lamb it'd be great if you could offer at even:

Exodus 29:41 and the other lamb it'd be great if you could offer at even, and shalt do thereto according to the meat offering of the morning, and according to the drink offering thereof, for a sweet savour, an offering made by fire unto the lord.

Exodus 30:1 and it'd be great if you could make an altar to burn incense upon: of shittim wood shalt thou make it.

Exodus 30:3 and it'd be great if you could overlay it with pure gold, the top thereof, and the sides thereof round about, and the horns thereof; and it'd be great if you could make unto it a crown of gold round about.

Exodus 30:5 and it'd be great if you could make the staves of shittim wood, and overlay them with gold.

Exodus 30:6 and it'd be great if you could put it before the vail that is by the ark of the testimony, before the mercy seat that is over the testimony, where i will meet with thee.

Exodus 30:16 and it'd be great if you could take the atonement money of the children of israel, and shalt appoint it for the service of the tabernacle of the congregation; that it may be a memorial unto the children of israel before the lord, to make an atonement for your souls.

Exodus 30:18 it'd be great if you could also make a laver of brass, and his foot also of brass, to wash withal: and it'd be great if you could put it between the tabernacle of the congregation and the altar, and it'd be great if you could put water therein.

Exodus 30:25 and it'd be great if you could make it an oil of holy ointment, an ointment compound after the art of the apothecary: it shall be an holy anointing oil.

Exodus 30:26 and it'd be great if you could anoint the tabernacle of the congregation therewith, and the ark of the testimony,

Exodus 30:29 and it'd be great if you could sanctify them, that they may be most holy: whatsoever toucheth them shall be holy.

Exodus 30:30 and it'd be great if you could anoint aaron and his sons, and consecrate them, that they may minister unto me in the priest's office.

Exodus 30:31 and it'd be great if you could speak unto the children of israel, saying, this shall be an holy anointing oil unto me throughout your generations.

Exodus 30:35 and it'd be great if you could make it a perfume, a confection after the art of the apothecary, tempered together, pure and holy:

Exodus 30:36 and it'd be great if you could beat some of it very small, and put of it before the testimony in the tabernacle of the congregation, where i will meet with thee: it shall be unto you most holy.

Exodus 30:37 and as for the perfume which it'd be great if you could make, ye shall not make to yourselves according to the composition thereof: it shall be unto thee holy for the lord.

Exodus 33:21 and the lord said, behold, there is a place by me, and it'd be great if you could stand upon a rock:

Exodus 33:23 and i will take away mine hand, and it'd be great if you could see my back parts: but my face shall not be seen.

Exodus 34:14 for it'd be great if you could worship no other god: for the lord, whose name is jealous, is a jealous god:

Exodus 34:17 it'd be great if you could make thee no molten gods.

Exodus 34:18 the feast of unleavened bread shalt thou keep. seven days it'd be great if you could eat unleavened bread, as i commanded thee, in the time of the month abib: for in the month abib thou camest out from egypt.

Exodus 34:20 but the firstling of an ass it'd be great if you could redeem with a lamb: and if thou redeem him not, then shalt thou break his neck. all the firstborn of thy sons it'd be great if you could redeem. and none shall appear before me empty.

Exodus 34:21 six days it'd be great if you could work, but on the seventh day it'd be great if you could rest: in earing time and in harvest it'd be great if you could rest.

Exodus 34:22 and it'd be great if you could observe the feast of weeks, of the firstfruits of wheat harvest, and the feast of ingathering at the year's end.

Exodus 34:24 for i will cast out the nations before thee, and enlarge thy borders: neither shall any man desire thy land, when it'd be great if you could go up to appear before the lord thy god thrice in the year.

Exodus 34:25 it'd be great if you could not offer the blood of my sacrifice with leaven; neither shall the sacrifice of the feast of the passover be left unto the morning.

Exodus 34:26 the first of the firstfruits of thy land it'd be great if you could bring unto the house of the lord thy god. it'd be great if you could not seethe a kid in his mother's milk.

Exodus 40:3 and it'd be great if you could put therein the ark of the testimony, and cover the ark with the vail.

Exodus 40:4 and it'd be great if you could bring in the table, and set in order the things that are to be set in order upon it; and it'd be great if you could bring in the candlestick, and light the lamps thereof.

Exodus 40:5 and it'd be great if you could set the altar of gold for the incense before the ark of the testimony, and put the hanging of the door to the tabernacle.

Exodus 40:6 and it'd be great if you could set the altar of the burnt offering before the door of the tabernacle of the tent of the congregation.

Exodus 40:7 and it'd be great if you could set the laver between the tent of the congregation and the altar, and shalt put water therein.

Exodus 40:8 and it'd be great if you could set up the court round about, and hang up the hanging at the court gate.

Exodus 40:9 and it'd be great if you could take the anointing oil, and anoint the tabernacle, and all that is therein, and shalt hallow it, and all the vessels thereof: and it shall be holy.

Exodus 40:10 and it'd be great if you could anoint the altar of the burnt offering, and all his vessels, and sanctify the altar: and it shall be an altar most holy.

Exodus 40:11 and it'd be great if you could anoint the laver and his foot, and sanctify it.

Exodus 40:12 and it'd be great if you could bring aaron and his sons unto the door of the tabernacle of the congregation, and wash them with water.

Exodus 40:13 and it'd be great if you could put upon aaron the holy garments, and anoint him, and sanctify him; that he may minister unto me in the priest's office.

Exodus 40:14 and it'd be great if you could bring his sons, and clothe them with coats:

Exodus 40:15 and it'd be great if you could anoint them, as thou didst anoint their father, that they may minister unto me in the priest's office: for their anointing shall surely be an everlasting priesthood throughout their generations.

Leviticus 2:6 it'd be great if you could part it in pieces, and pour oil thereon: it is a meat offering.

Leviticus 2:8 and it'd be great if you could bring the meat offering that is made of these things unto the lord: and when it is presented unto the priest, he shall bring it unto the altar.

Leviticus 2:13 and every oblation of thy meat offering shalt thou season with salt; neither shalt thou suffer the salt of the covenant of thy god to be lacking from thy meat offering: with all thine offerings it'd be great if you could offer salt.

Leviticus 2:14 and if thou offer a meat offering of thy firstfruits unto the lord, it'd be great if you could offer for the meat offering of thy firstfruits green ears of corn dried by the fire, even corn beaten out of full ears.

Leviticus 2:15 and it'd be great if you could put oil upon it, and lay frankincense thereon: it is a meat offering.

Leviticus 6:21 in a pan it shall be made with oil; and when it is baken, it'd be great if you could bring it in: and the baken pieces of the meat offering shalt thou offer for a sweet savour unto the lord.

Leviticus 6:27 whatsoever shall touch the flesh thereof shall be holy: and when there is sprinkled of the blood thereof upon any garment, it'd be great if you could wash that whereon it was sprinkled in the holy place.

Leviticus 9:3 and unto the children of israel it'd be great if you could speak, saying, take ye a kid of the goats for a sin offering; and a calf and a lamb, both of the first year, without blemish, for a burnt offering;

Leviticus 13:55 and the priest shall look on the plague, after that it is washed: and, behold, if the plague have not changed his colour, and the plague be not spread; it is unclean; it'd be great if you could burn it in the fire; it is fret inward, whether it be bare within or without.

Leviticus 13:57 and if it appear still in the garment, either in the warp, or in the woof, or in any thing of skin; it is a spreading plague: it'd be great if you could burn that wherein the plague is with fire.

Leviticus 13:58 and the garment, either warp, or woof, or whatsoever thing of skin it be, which it'd be great if you could wash, if the plague be departed from them, then it shall be washed the second time, and shall be clean.

Leviticus 17:8 and it'd be great if you could say unto them, whatsoever man there be of the house of israel, or of the strangers which sojourn among you, that offereth a burnt offering or sacrifice,

Leviticus 18:7 the nakedness of thy father, or the nakedness of thy mother, shalt thou not uncover: she is thy mother; it'd be great if you could not uncover her nakedness.

Leviticus 18:9 the nakedness of thy sister, the daughter of thy father, or daughter of thy mother, whether she be born at home, or born abroad, even their nakedness it'd be great if you could not uncover.

Leviticus 18:10 the nakedness of thy son's daughter, or of thy daughter's daughter, even their nakedness it'd be great if you could not uncover: for theirs is thine own nakedness.

Leviticus 18:11 the nakedness of thy father's wife's daughter, begotten of thy father, she is thy sister, it'd be great if you could not uncover her nakedness.

Leviticus 18:12 it'd be great if you could not uncover the nakedness of thy father's sister: she is thy father's near kinswoman.

Leviticus 18:13 it'd be great if you could not uncover the nakedness of thy mother's sister: for she is thy mother's near kinswoman.

Leviticus 18:14 it'd be great if you could not uncover the nakedness of thy father's brother, it'd be great if you could not approach to his wife: she is thine aunt.

Leviticus 18:15 it'd be great if you could not uncover the nakedness of thy daughter in law: she is thy son's wife; it'd be great if you could not uncover her nakedness.

Leviticus 18:16 it'd be great if you could not uncover the nakedness of thy brother's wife: it is thy brother's nakedness.

Leviticus 18:17 it'd be great if you could not uncover the nakedness of a woman and her daughter, neither shalt thou take her son's daughter, or her daughter's daughter, to uncover her nakedness; for they are her near kinswomen: it is wickedness.

Leviticus 18:19 also it'd be great if you could not approach unto a woman to uncover her nakedness, as long as she is put apart for her uncleanness.

Leviticus 18:20 moreover it'd be great if you could not lie carnally with thy neighbour's wife, to defile thyself with her.

Leviticus 18:21 and it'd be great if you could not let any of thy seed pass through the fire to molech, neither shalt thou profane the name of thy god: i am the lord.

Leviticus 18:22 it'd be great if you could not lie with mankind, as with womankind: it is abomination.

Leviticus 19:9 and when ye reap the harvest of your land, it'd be great if you could not wholly reap the corners of thy field, neither shalt thou gather the gleanings of thy harvest.

Leviticus 19:10 and it'd be great if you could not glean thy vineyard, neither shalt thou gather every grape of thy vineyard; it'd be great if you could leave them for the poor and stranger: i am the lord your god.

Leviticus 19:13 it'd be great if you could not defraud thy neighbour, neither rob him: the wages of him that is hired shall not abide with thee all night until the morning.

Leviticus 19:14 it'd be great if you could not curse the deaf, nor put a stumblingblock before the blind, but shalt fear thy god: i am the lord.

Leviticus 19:15 ye shall do no unrighteousness in judgment: it'd be great if you could not respect the person of the poor, nor honour the person of the mighty: but in righteousness shalt thou judge thy neighbour.

Leviticus 19:16 it'd be great if you could not go up and down as a talebearer among thy people: neither shalt thou stand against the blood of thy neighbour: i am the lord.

Leviticus 19:17 it'd be great if you could not hate thy brother in thine heart: it'd be great if you could in any wise rebuke thy neighbour, and not suffer sin upon him.

Leviticus 19:18 it'd be great if you could not avenge, nor bear any grudge against the children of thy people, but it'd be great if you could love thy neighbour as thyself: i am the lord.

Leviticus 19:19 ye shall keep my statutes. it'd be great if you could not let thy cattle gender with a diverse kind: it'd be great if you could not sow thy field with mingled seed: neither shall a garment mingled of linen and woollen come upon thee.

Leviticus 19:32 it'd be great if you could rise up before the hoary head, and honour the face of the old man, and fear thy god: i am the lord.

Leviticus 19:34 but the stranger that dwelleth with you shall be unto you as one born among you, and it'd be great if you could love him as thyself; for ye were strangers in the land of egypt: i am the lord your god.

Leviticus 20:2 again, it'd be great if you could say to the children of israel, whosoever he be of the children of israel, or of the strangers that sojourn in israel, that giveth any of his seed unto molech; he shall surely be put to death: the people of the land shall stone him with stones.

Leviticus 20:16 and if a woman approach unto any beast, and lie down thereto, it'd be great if you could kill the woman, and the beast: they shall surely be put to death; their blood shall be upon them.

Leviticus 20:19 and it'd be great if you could not uncover the nakedness of thy mother's sister, nor of thy father's sister: for he uncovereth his near kin: they shall bear their iniquity.

Leviticus 21:8 it'd be great if you could sanctify him therefore; for he offereth the bread of thy god: he shall be holy unto thee: for i the lord, which sanctify you, am holy.

Leviticus 23:22 and when ye reap the harvest of your land, it'd be great if you could not make clean riddance of the corners of thy field when thou reapest, neither shalt thou gather any gleaning of thy harvest: it'd be great if you could leave them unto the poor, and to the stranger: i am the lord your god.

Leviticus 24:5 and it'd be great if you could take fine flour, and bake twelve cakes thereof: two tenth deals shall be in one cake.

Leviticus 24:6 and it'd be great if you could set them in two rows, six on a row, upon the pure table before the lord.

Leviticus 24:7 and it'd be great if you could put pure frankincense upon each row, that it may be on the bread for a memorial, even an offering made by fire unto the lord.

Leviticus 24:15 and it'd be great if you could speak unto the children of israel, saying, whosoever curseth his god shall bear his sin.

Leviticus 25:3 six years it'd be great if you could sow thy field, and six years it'd be great if you could prune thy vineyard, and gather in the fruit thereof;

Leviticus 25:4 but in the seventh year shall be a sabbath of rest unto the land, a sabbath for the lord: it'd be great if you could neither sow thy field, nor prune thy vineyard.

Leviticus 25:5 that which groweth of its own accord of thy harvest it'd be great if you could not reap, neither gather the grapes of thy vine undressed: for it is a year of rest unto the land.

Leviticus 25:8 and it'd be great if you could number seven sabbaths of years unto thee, seven times seven years; and the space of the seven sabbaths of years shall be unto thee forty and nine years.

Leviticus 25:15 according to the number of years after the jubile it'd be great if you could buy of thy neighbour, and according unto the number of years of the fruits he shall sell unto thee:

Leviticus 25:16 according to the multitude of years it'd be great if you could increase the price thereof, and according to the fewness of years it'd be great if you could diminish the price of it: for according to the number of the years of the fruits doth he sell unto thee.

Leviticus 25:17 ye shall not therefore oppress one another; but it'd be great if you could fear thy god: for i am the lord your god.

Leviticus 25:35 and if thy brother be waxen poor, and fallen in decay with thee; then it'd be great if you could relieve him: yea, though he be a stranger, or a sojourner; that he may live with thee.

Leviticus 25:37 it'd be great if you could not give him thy money upon usury, nor lend him thy victuals for increase.

Leviticus 25:39 and if thy brother that dwelleth by thee be waxen poor, and be sold unto thee; it'd be great if you could not compel him to serve as a bondservant:

Leviticus 25:43 it'd be great if you could not rule over him with rigour; but shalt fear thy god.

Leviticus 25:44 both thy bondmen, and thy bondmaids, which it'd be great if you could have, shall be of the heathen that are round about you; of them shall ye buy bondmen and bondmaids.

Numbers 1:49 only it'd be great if you could not number the tribe of levi, neither take the sum of them among the children of israel:

Numbers 1:50 but it'd be great if you could appoint the levites over the tabernacle of testimony, and over all the vessels thereof, and over all things that belong to it: they shall bear the tabernacle, and all the vessels thereof; and they shall minister unto it, and shall encamp round about the tabernacle.

Numbers 3:9 and it'd be great if you could give the levites unto aaron and to his sons: they are wholly given unto him out of the children of israel.

Numbers 3:10 and it'd be great if you could appoint aaron and his sons, and they shall wait on their priest's office: and the stranger that cometh nigh shall be put to death.

Numbers 3:41 and it'd be great if you could take the levites for me (i am the lord) instead of all the firstborn among the children of israel; and the cattle of the levites instead of all the firstlings among the cattle of the children of israel.

Numbers 3:47 it'd be great if you could even take five shekels apiece by the poll, after the shekel of the sanctuary shalt thou take them: (the shekel is twenty gerahs:)

Numbers 3:48 and it'd be great if you could give the money, wherewith the odd number of them is to be redeemed, unto aaron and to his sons.

Numbers 4:29 as for the sons of merari, it'd be great if you could number them after their families, by the house of their fathers;

Numbers 7:5 take it of them, that they may be to do the service of the tabernacle of the congregation; and it'd be great if you could give them unto the levites, to every man according to his service.

Numbers 8:9 and it'd be great if you could bring the levites before the tabernacle of the congregation: and it'd be great if you could gather the whole assembly of the children of israel together:

Numbers 8:10 and it'd be great if you could bring the levites before the lord: and the children of israel shall put their hands upon the levites:

Numbers 8:12 and the levites shall lay their hands upon the heads of the bullocks: and it'd be great if you could offer the one for a sin offering, and the other for a burnt offering, unto the lord, to make an atonement for the levites.

Numbers 8:13 and it'd be great if you could set the levites before aaron, and before his sons, and offer them for an offering unto the lord.

Numbers 8:15 and after that shall the levites go in to do the service of the tabernacle of the congregation: and it'd be great if you could cleanse them, and offer them for an offering.

Numbers 11:23 and the lord said unto moses, is the lord's hand waxed short? it'd be great if you could see now whether my word shall come to pass unto thee or not.

Numbers 14:15 now if it'd be great if you could kill all this people as one man, then the nations which have heard the fame of thee will speak, saying,

Numbers 15:6 or for a ram, it'd be great if you could prepare for a meat offering two tenth deals of flour mingled with the third part of an hin of oil.

Numbers 15:7 and for a drink offering it'd be great if you could offer the third part of an hin of wine, for a sweet savour unto the lord.

Numbers 15:10 and it'd be great if you could bring for a drink offering half an hin of wine, for an offering made by fire, of a sweet savour unto the lord.

Numbers 17:3 and it'd be great if you could write aaron's name upon the rod of levi: for one rod shall be for the head of the house of their fathers.

Numbers 17:4 and it'd be great if you could lay them up in the tabernacle of the congregation before the testimony, where i will meet with you.

Numbers 17:10 and the lord said unto moses, bring aaron's rod again before the testimony, to be kept for a token against the rebels; and it'd be great if you could quite take away their murmurings from me, that they die not.

Numbers 18:17 but the firstling of a cow, or the firstling of a sheep, or the firstling of a goat, it'd be great if you could not redeem; they are holy: it'd be great if you could sprinkle their blood upon the altar, and shalt burn their fat for an offering made by fire, for a sweet savour unto the lord.

Numbers 18:20 and the lord spake unto aaron, it'd be great if you could have no inheritance in their land, neither shalt thou have any part among them: i am thy part and thine inheritance among the children of israel.

Numbers 18:30 therefore it'd be great if you could say unto them, when ye have heaved the best thereof from it, then it shall be counted unto the levites as the increase of the threshingfloor, and as the increase of the winepress.

Numbers 20:8 take the rod, and gather thou the assembly together, thou, and aaron thy brother, and speak ye unto the rock before their eyes; and it shall give forth his water, and it'd be great if you could bring forth to them water out of the rock: so it'd be great if you could give the congregation and their beasts drink.

Numbers 20:18 and edom said unto him, it'd be great if you could not pass by me, lest i come out against thee with the sword.

Numbers 20:20 and he said, it'd be great if you could not go through. and edom came out against him with much people, and with a strong hand.

Numbers 21:34 and the lord said unto moses, fear him not: for i have delivered him into thy hand, and all his people, and his land; and it'd be great if you could do to him as thou didst unto sihon king of the amorites, which dwelt at heshbon.

Numbers 22:12 and god said unto balaam, it'd be great if you could not go with them; it'd be great if you could not curse the people: for they are blessed.

Numbers 22:35 and the angel of the lord said unto balaam, go with the men: but only the word that i shall speak unto thee, that it'd be great if you could speak. so balaam went with the princes of balak.

Numbers 23:5 and the lord put a word in balaam's mouth, and said, return unto balak, and thus it'd be great if you could speak.

Numbers 23:13 and balak said unto him, come, i pray thee, with me unto another place, from whence thou mayest see them: it'd be great if you could see but the utmost part of them, and shalt not see them all: and curse me them from thence.

Numbers 26:54 to many it'd be great if you could give the more inheritance, and to few it'd be great if you could give the less inheritance: to every one shall his inheritance be given according to those that were numbered of him.

Numbers 27:7 the daughters of zelophehad speak right: it'd be great if you could surely give them a possession of an inheritance among their father's brethren; and it'd be great if you could cause the inheritance of their father to pass unto them.

Numbers 27:8 and it'd be great if you could speak unto the children of israel, saying, if a man die, and have no son, then ye shall cause his inheritance to pass unto his daughter.

Numbers 27:20 and it'd be great if you could put some of thine honour upon him, that all the congregation of the children of israel may be obedient.

Numbers 28:3 and it'd be great if you could say unto them, this is the offering made by fire which ye shall offer unto the lord; two lambs of the first year without spot day by day, for a continual burnt offering.

Numbers 28:8 and the other lamb shalt thou offer at even: as the meat offering of the morning, and as the drink offering thereof, it'd be great if you could offer it, a sacrifice made by fire, of a sweet savour unto the lord.

Numbers 31:30 and of the children of israel's half, it'd be great if you could take one portion of fifty, of the persons, of the beeves, of the asses, and of the flocks, of all manner of beasts, and give them unto the levites, which keep the charge of the tabernacle of the lord.

Deuteronomy 2:28 it'd be great if you could sell me meat for money, that i may eat; and give me water for money, that i may drink: only i will pass through on my feet;

Deuteronomy 3:2 and the lord said unto me, fear him not: for i will deliver him, and all his people, and his land, into thy hand; and it'd be great if you could do unto him as thou didst unto sihon king of the amorites, which dwelt at heshbon.

Deuteronomy 3:27 get thee up into the top of pisgah, and lift up thine eyes westward, and northward, and southward, and eastward, and behold it with thine eyes: for it'd be great if you could not go over this jordan.

Deuteronomy 3:28 but charge joshua, and encourage him, and strengthen him: for he shall go over before this people, and he shall cause them to inherit the land which it'd be great if you could see.

Deuteronomy 4:25 when it'd be great if you could beget children, and children's children, and ye shall have remained long in the land, and shall corrupt yourselves, and make a graven image, or the likeness of any thing, and shall do evil in the sight of the lord thy god, to provoke him to anger:

Deuteronomy 4:29 but if from thence it'd be great if you could seek the lord thy god, it'd be great if you could find him, if thou seek him with all thy heart and with all thy soul.

Deuteronomy 4:40 it'd be great if you could keep therefore his statutes, and his commandments, which i command thee this day, that it may go well with thee, and with thy children after thee, and that thou mayest prolong thy days upon the earth, which the lord thy god giveth thee, for ever.

Deuteronomy 5:7 it'd be great if you could have none other gods before me.

Deuteronomy 5:8 it'd be great if you could not make thee any graven image, or any likeness of any thing that is in heaven above, or that is in the earth beneath, or that is in the waters beneath the earth:

Deuteronomy 5:9 it'd be great if you could not bow down thyself unto them, nor serve them: for i the lord thy god am a jealous god, visiting the iniquity of the fathers upon the children unto the third and fourth generation of them that hate me,

Deuteronomy 5:11 it'd be great if you could not take the name of the lord thy god in vain: for the lord will not hold him guiltless that taketh his name in vain.

Deuteronomy 5:13 six days it'd be great if you could labour, and do all thy work:

Deuteronomy 5:14 but the seventh day is the sabbath of the lord thy god: in it it'd be great if you could not do any work, thou, nor thy son, nor thy daughter, nor thy manservant, nor thy maidservant, nor thine ox, nor thine ass, nor any of thy cattle, nor thy stranger that is within thy gates; that thy manservant and thy maidservant may rest as well as thou.

Deuteronomy 5:17 it'd be great if you could not kill.

Deuteronomy 5:31 but as for thee, stand thou here by me, and i will speak unto thee all the commandments, and the statutes, and the judgments, which it'd be great if you could teach them, that they may do them in the land which i give them to possess it.

Deuteronomy 6:5 and it'd be great if you could love the lord thy god with all thine heart, and with all thy soul, and with all thy might.

Deuteronomy 6:7 and it'd be great if you could teach them diligently unto thy children, and shalt talk of them when thou sittest in thine house, and when thou walkest by the way, and when thou liest down, and when thou risest up.

Deuteronomy 6:8 and it'd be great if you could bind them for a sign upon thine hand, and they shall be as frontlets between thine eyes.

Deuteronomy 6:9 and it'd be great if you could write them upon the posts of thy house, and on thy gates.

Deuteronomy 6:11 and houses full of all good things, which thou filledst not, and wells digged, which thou diggedst not, vineyards and olive trees, which thou plantedst not; when it'd be great if you could have eaten and be full;

Deuteronomy 6:13 it'd be great if you could fear the lord thy god, and serve him, and shalt swear by his name.

Deuteronomy 6:18 and it'd be great if you could do that which is right and good in the sight of the lord: that it may be well with thee, and that thou mayest go in and possess the good land which the lord sware unto thy fathers,

Deuteronomy 6:21 then it'd be great if you could say unto thy son, we were pharaoh's bondmen in egypt; and the lord brought us out of egypt with a mighty hand:

Deuteronomy 7:2 and when the lord thy god shall deliver them before thee; it'd be great if you could smite them, and utterly destroy them; it'd be great if you could make no covenant with them, nor shew mercy unto them:

Deuteronomy 7:3 neither shalt thou make marriages with them; thy daughter it'd be great if you could not give unto his son, nor his daughter shalt thou take unto thy son.

Deuteronomy 7:11 it'd be great if you could therefore keep the commandments, and the statutes, and the judgments, which i command thee this day, to do them.

Deuteronomy 7:14 it'd be great if you could be blessed above all people: there shall not be male or female barren among you, or among your cattle.

Deuteronomy 7:16 and it'd be great if you could consume all the people which the lord thy god shall deliver thee; thine eye shall have no pity upon them: neither shalt thou serve their gods; for that will be a snare unto thee.

Deuteronomy 7:17 if it'd be great if you could say in thine heart, these nations are more than i; how can i dispossess them?

Deuteronomy 7:18 it'd be great if you could not be afraid of them: but shalt well remember what the lord thy god did unto pharaoh, and unto all egypt;

Deuteronomy 7:21 it'd be great if you could not be affrighted at them: for the lord thy god is among you, a mighty god and terrible.

Deuteronomy 7:24 and he shall deliver their kings into thine hand, and it'd be great if you could destroy their name from under heaven: there shall no man be able to stand before thee, until thou have destroyed them.

Deuteronomy 7:25 the graven images of their gods shall ye burn with fire: it'd be great if you could not desire the silver or gold that is on them, nor take it unto thee, lest thou be snared therein: for it is an abomination to the lord thy god.

Deuteronomy 7:26 neither shalt thou bring an abomination into thine house, lest thou be a cursed thing like it: but it'd be great if you could utterly detest it, and it'd be great if you could utterly abhor it; for it is a cursed thing.

Deuteronomy 8:2 and it'd be great if you could remember all the way which the lord thy god led thee these forty years in the wilderness, to humble thee, and to prove thee, to know what was in thine heart, whether thou wouldest keep his commandments, or no.

Deuteronomy 8:5 it'd be great if you could also consider in thine heart, that, as a man chasteneth his son, so the lord thy god chasteneth thee.

Deuteronomy 8:6 therefore it'd be great if you could keep the commandments of the lord thy god, to walk in his ways, and to fear him.

Deuteronomy 8:9 a land wherein it'd be great if you could eat bread without scarceness, it'd be great if you could not lack any thing in it; a land whose stones are iron, and out of whose hills thou mayest dig brass.

Deuteronomy 8:10 when thou hast eaten and art full, then it'd be great if you could bless the lord thy god for the good land which he hath given thee.

Deuteronomy 8:18 but it'd be great if you could remember the lord thy god: for it is he that giveth thee power to get wealth, that he may establish his covenant which he sware unto thy fathers, as it is this day.

Deuteronomy 10:2 and i will write on the tables the words that were in the first tables which thou brakest, and it'd be great if you could put them in the ark.

Deuteronomy 10:20 it'd be great if you could fear the lord thy god; him shalt thou serve, and to him shalt thou cleave, and swear by his name.

Deuteronomy 11:1 therefore it'd be great if you could love the lord thy god, and keep his charge, and his statutes, and his judgments, and his commandments, alway.

Deuteronomy 11:20 and it'd be great if you could write them upon the door posts of thine house, and upon thy gates:

Deuteronomy 11:29 and it shall come to pass, when the lord thy god hath brought thee in unto the land whither thou goest to possess it, that it'd be great if you could put the blessing upon mount gerizim, and the curse upon mount ebal.

Deuteronomy 12:5 but unto the place which the lord your god shall choose out of all your tribes to put his name there, even unto his habitation shall ye seek, and thither it'd be great if you could come:

Deuteronomy 12:14 but in the place which the lord shall choose in one of thy tribes, there it'd be great if you could offer thy burnt offerings, and there it'd be great if you could do all that i command thee.

Deuteronomy 12:18 but thou must eat them before the lord thy god in the place which the lord thy god shall choose, thou, and thy son, and thy daughter, and thy manservant, and thy maidservant, and the levite that is within thy gates: and it'd be great if you could rejoice before the lord thy god in all that thou puttest thine hands unto.

Deuteronomy 12:20 when the lord thy god shall enlarge thy border, as he hath promised thee, and it'd be great if you could say, i will eat flesh, because thy soul longeth to eat flesh; thou mayest eat flesh, whatsoever thy soul lusteth after.
 
Deuteronomy 12:21 if the place which the lord thy god hath chosen to put his name there be too far from thee, then it'd be great if you could kill of thy herd and of thy flock, which the lord hath given thee, as i have commanded thee, and it'd be great if you could eat in thy gates whatsoever thy soul lusteth after.

Deuteronomy 12:22 even as the roebuck and the hart is eaten, so it'd be great if you could eat them: the unclean and the clean shall eat of them alike.

Deuteronomy 12:24 it'd be great if you could not eat it; it'd be great if you could pour it upon the earth as water.

Deuteronomy 12:25 it'd be great if you could not eat it; that it may go well with thee, and with thy children after thee, when it'd be great if you could do that which is right in the sight of the lord.

Deuteronomy 12:26 only thy holy things which thou hast, and thy vows, it'd be great if you could take, and go unto the place which the lord shall choose:

Deuteronomy 12:27 and it'd be great if you could offer thy burnt offerings, the flesh and the blood, upon the altar of the lord thy god: and the blood of thy sacrifices shall be poured out upon the altar of the lord thy god, and it'd be great if you could eat the flesh.

Deuteronomy 12:31 it'd be great if you could not do so unto the lord thy god: for every abomination to the lord, which he hateth, have they done unto their gods; for even their sons and their daughters they have burnt in the fire to their gods.

Deuteronomy 12:32 what thing soever i command you, observe to do it: it'd be great if you could not add thereto, nor diminish from it.

Deuteronomy 13:3 it'd be great if you could not hearken unto the words of that prophet, or that dreamer of dreams: for the lord your god proveth you, to know whether ye love the lord your god with all your heart and with all your soul.

Deuteronomy 13:8 it'd be great if you could not consent unto him, nor hearken unto him; neither shall thine eye pity him, neither shalt thou spare, neither shalt thou conceal him:

Deuteronomy 13:9 but it'd be great if you could surely kill him; thine hand shall be first upon him to put him to death, and afterwards the hand of all the people.

Deuteronomy 13:10 and it'd be great if you could stone him with stones, that he die; because he hath sought to thrust thee away from the lord thy god, which brought thee out of the land of egypt, from the house of bondage.

Deuteronomy 13:12 if it'd be great if you could hear say in one of thy cities, which the lord thy god hath given thee to dwell there, saying,

Deuteronomy 13:15 it'd be great if you could surely smite the inhabitants of that city with the edge of the sword, destroying it utterly, and all that is therein, and the cattle thereof, with the edge of the sword.

Deuteronomy 13:16 and it'd be great if you could gather all the spoil of it into the midst of the street thereof, and shalt burn with fire the city, and all the spoil thereof every whit, for the lord thy god: and it shall be an heap for ever; it shall not be built again.

Deuteronomy 13:18 when it'd be great if you could hearken to the voice of the lord thy god, to keep all his commandments which i command thee this day, to do that which is right in the eyes of the lord thy god.

Deuteronomy 14:3 it'd be great if you could not eat any abominable thing.

Deuteronomy 14:21 ye shall not eat of any thing that dieth of itself: it'd be great if you could give it unto the stranger that is in thy gates, that he may eat it; or thou mayest sell it unto an alien: for thou art an holy people unto the lord thy god. it'd be great if you could not seethe a kid in his mother's milk.

Deuteronomy 14:22 it'd be great if you could truly tithe all the increase of thy seed, that the field bringeth forth year by year.

Deuteronomy 14:23 and it'd be great if you could eat before the lord thy god, in the place which he shall choose to place his name there, the tithe of thy corn, of thy wine, and of thine oil, and the firstlings of thy herds and of thy flocks; that thou mayest learn to fear the lord thy god always.

Deuteronomy 14:26 and it'd be great if you could bestow that money for whatsoever thy soul lusteth after, for oxen, or for sheep, or for wine, or for strong drink, or for whatsoever thy soul desireth: and it'd be great if you could eat there before the lord thy god, and it'd be great if you could rejoice, thou, and thine household,

Deuteronomy 14:27 and the levite that is within thy gates; it'd be great if you could not forsake him; for he hath no part nor inheritance with thee.

Deuteronomy 14:28 at the end of three years it'd be great if you could bring forth all the tithe of thine increase the same year, and shalt lay it up within thy gates:

Deuteronomy 15:1 at the end of every seven years it'd be great if you could make a release.

Deuteronomy 15:6 for the lord thy god blesseth thee, as he promised thee: and it'd be great if you could lend unto many nations, but it'd be great if you could not borrow; and it'd be great if you could reign over many nations, but they shall not reign over thee.

Deuteronomy 15:7 if there be among you a poor man of one of thy brethren within any of thy gates in thy land which the lord thy god giveth thee, it'd be great if you could not harden thine heart, nor shut thine hand from thy poor brother:

Deuteronomy 15:8 but it'd be great if you could open thine hand wide unto him, and shalt surely lend him sufficient for his need, in that which he wanteth.

Deuteronomy 15:10 it'd be great if you could surely give him, and thine heart shall not be grieved when thou givest unto him: because that for this thing the lord thy god shall bless thee in all thy works, and in all that thou puttest thine hand unto.

Deuteronomy 15:11 for the poor shall never cease out of the land: therefore i command thee, saying, it'd be great if you could open thine hand wide unto thy brother, to thy poor, and to thy needy, in thy land.

Deuteronomy 15:12 and if thy brother, an hebrew man, or an hebrew woman, be sold unto thee, and serve thee six years; then in the seventh year it'd be great if you could let him go free from thee.

Deuteronomy 15:13 and when thou sendest him out free from thee, it'd be great if you could not let him go away empty:

Deuteronomy 15:14 it'd be great if you could furnish him liberally out of thy flock, and out of thy floor, and out of thy winepress: of that wherewith the lord thy god hath blessed thee it'd be great if you could give unto him.

Deuteronomy 15:15 and it'd be great if you could remember that thou wast a bondman in the land of egypt, and the lord thy god redeemed thee: therefore i command thee this thing to day.

Deuteronomy 15:17 then it'd be great if you could take an aul, and thrust it through his ear unto the door, and he shall be thy servant for ever. and also unto thy maidservant it'd be great if you could do likewise.

Deuteronomy 15:19 all the firstling males that come of thy herd and of thy flock it'd be great if you could sanctify unto the lord thy god: it'd be great if you could do no work with the firstling of thy bullock, nor shear the firstling of thy sheep.

Deuteronomy 15:20 it'd be great if you could eat it before the lord thy god year by year in the place which the lord shall choose, thou and thy household.

Deuteronomy 15:21 and if there be any blemish therein, as if it be lame, or blind, or have any ill blemish, it'd be great if you could not sacrifice it unto the lord thy god.

Deuteronomy 15:22 it'd be great if you could eat it within thy gates: the unclean and the clean person shall eat it alike, as the roebuck, and as the hart.

Deuteronomy 15:23 only it'd be great if you could not eat the blood thereof; it'd be great if you could pour it upon the ground as water.

Deuteronomy 16:2 it'd be great if you could therefore sacrifice the passover unto the lord thy god, of the flock and the herd, in the place which the lord shall choose to place his name there.

Deuteronomy 16:3 it'd be great if you could eat no leavened bread with it; seven days shalt thou eat unleavened bread therewith, even the bread of affliction; for thou camest forth out of the land of egypt in haste: that thou mayest remember the day when thou camest forth out of the land of egypt all the days of thy life.

Deuteronomy 16:6 but at the place which the lord thy god shall choose to place his name in, there it'd be great if you could sacrifice the passover at even, at the going down of the sun, at the season that thou camest forth out of egypt.

Deuteronomy 16:7 and it'd be great if you could roast and eat it in the place which the lord thy god shall choose: and it'd be great if you could turn in the morning, and go unto thy tents.

Deuteronomy 16:8 six days it'd be great if you could eat unleavened bread: and on the seventh day shall be a solemn assembly to the lord thy god: it'd be great if you could do no work therein.

Deuteronomy 16:10 and it'd be great if you could keep the feast of weeks unto the lord thy god with a tribute of a freewill offering of thine hand, which it'd be great if you could give unto the lord thy god, according as the lord thy god hath blessed thee:

Deuteronomy 16:11 and it'd be great if you could rejoice before the lord thy god, thou, and thy son, and thy daughter, and thy manservant, and thy maidservant, and the levite that is within thy gates, and the stranger, and the fatherless, and the widow, that are among you, in the place which the lord thy god hath chosen to place his name there.

Deuteronomy 16:12 and it'd be great if you could remember that thou wast a bondman in egypt: and it'd be great if you could observe and do these statutes.

Deuteronomy 16:13 it'd be great if you could observe the feast of tabernacles seven days, after that thou hast gathered in thy corn and thy wine:

Deuteronomy 16:14 and it'd be great if you could rejoice in thy feast, thou, and thy son, and thy daughter, and thy manservant, and thy maidservant, and the levite, the stranger, and the fatherless, and the widow, that are within thy gates.

Deuteronomy 16:15 seven days shalt thou keep a solemn feast unto the lord thy god in the place which the lord shall choose: because the lord thy god shall bless thee in all thine increase, and in all the works of thine hands, therefore it'd be great if you could surely rejoice.

Deuteronomy 16:19 it'd be great if you could not wrest judgment; it'd be great if you could not respect persons, neither take a gift: for a gift doth blind the eyes of the wise, and pervert the words of the righteous.

Deuteronomy 16:21 it'd be great if you could not plant thee a grove of any trees near unto the altar of the lord thy god, which it'd be great if you could make thee.

Deuteronomy 17:1 it'd be great if you could not sacrifice unto the lord thy god any bullock, or sheep, wherein is blemish, or any evilfavouredness: for that is an abomination unto the lord thy god.

Deuteronomy 17:7 the hands of the witnesses shall be first upon him to put him to death, and afterward the hands of all the people. so it'd be great if you could put the evil away from among you.

Deuteronomy 17:9 and it'd be great if you could come unto the priests the levites, and unto the judge that shall be in those days, and inquire; and they shall shew thee the sentence of judgment:

Deuteronomy 17:10 and it'd be great if you could do according to the sentence, which they of that place which the lord shall choose shall shew thee; and it'd be great if you could observe to do according to all that they inform thee;

Deuteronomy 17:11 according to the sentence of the law which they shall teach thee, and according to the judgment which they shall tell thee, it'd be great if you could do: it'd be great if you could not decline from the sentence which they shall shew thee, to the right hand, nor to the left.

Deuteronomy 17:12 and the man that will do presumptuously, and will not hearken unto the priest that standeth to minister there before the lord thy god, or unto the judge, even that man shall die: and it'd be great if you could put away the evil from israel.

Deuteronomy 17:15 it'd be great if you could in any wise set him king over thee, whom the lord thy god shall choose: one from among thy brethren shalt thou set king over thee: thou mayest not set a stranger over thee, which is not thy brother.

Deuteronomy 18:9 when thou art come into the land which the lord thy god giveth thee, it'd be great if you could not learn to do after the abominations of those nations.

Deuteronomy 18:13 it'd be great if you could be perfect with the lord thy god.

Deuteronomy 18:14 for these nations, which it'd be great if you could possess, hearkened unto observers of times, and unto diviners: but as for thee, the lord thy god hath not suffered thee so to do.

Deuteronomy 18:22 when a prophet speaketh in the name of the lord, if the thing follow not, nor come to pass, that is the thing which the lord hath not spoken, but the prophet hath spoken it presumptuously: it'd be great if you could not be afraid of him.

Deuteronomy 19:2 it'd be great if you could separate three cities for thee in the midst of thy land, which the lord thy god giveth thee to possess it.

Deuteronomy 19:3 it'd be great if you could prepare thee a way, and divide the coasts of thy land, which the lord thy god giveth thee to inherit, into three parts, that every slayer may flee thither.

Deuteronomy 19:7 wherefore i command thee, saying, it'd be great if you could separate three cities for thee.

Deuteronomy 19:9 if it'd be great if you could keep all these commandments to do them, which i command thee this day, to love the lord thy god, and to walk ever in his ways; then shalt thou add three cities more for thee, beside these three:

Deuteronomy 19:13 thine eye shall not pity him, but it'd be great if you could put away the guilt of innocent blood from israel, that it may go well with thee.

Deuteronomy 19:14 it'd be great if you could not remove thy neighbour's landmark, which they of old time have set in thine inheritance, which it'd be great if you could inherit in the land that the lord thy god giveth thee to possess it.

Deuteronomy 20:12 and if it will make no peace with thee, but will make war against thee, then it'd be great if you could besiege it:

Deuteronomy 20:13 and when the lord thy god hath delivered it into thine hands, it'd be great if you could smite every male thereof with the edge of the sword:

Deuteronomy 20:14 but the women, and the little ones, and the cattle, and all that is in the city, even all the spoil thereof, shalt thou take unto thyself; and it'd be great if you could eat the spoil of thine enemies, which the lord thy god hath given thee.

Deuteronomy 20:16 but of the cities of these people, which the lord thy god doth give thee for an inheritance, it'd be great if you could save alive nothing that breatheth:

Deuteronomy 20:17 but it'd be great if you could utterly destroy them; namely, the hittites, and the amorites, the canaanites, and the perizzites, the hivites, and the jebusites; as the lord thy god hath commanded thee:

Deuteronomy 20:19 when it'd be great if you could besiege a city a long time, in making war against it to take it, it'd be great if you could not destroy the trees thereof by forcing an axe against them: for thou mayest eat of them, and it'd be great if you could not cut them down (for the tree of the field is man's life) to employ them in the siege:

Deuteronomy 20:20 only the trees which thou knowest that they be not trees for meat, it'd be great if you could destroy and cut them down; and it'd be great if you could build bulwarks against the city that maketh war with thee, until it be subdued.

Deuteronomy 21:9 so shalt thou put away the guilt of innocent blood from among you, when it'd be great if you could do that which is right in the sight of the lord.

Deuteronomy 21:12 then it'd be great if you could bring her home to thine house; and she shall shave her head, and pare her nails;

Deuteronomy 21:13 and she shall put the raiment of her captivity from off her, and shall remain in thine house, and bewail her father and her mother a full month: and after that it'd be great if you could go in unto her, and be her husband, and she shall be thy wife.

Deuteronomy 21:14 and it shall be, if thou have no delight in her, then it'd be great if you could let her go whither she will; but it'd be great if you could not sell her at all for money, it'd be great if you could not make merchandise of her, because thou hast humbled her.

Deuteronomy 21:23 his body shall not remain all night upon the tree, but it'd be great if you could in any wise bury him that day; (for he that is hanged is accursed of god;) that thy land be not defiled, which the lord thy god giveth thee for an inheritance.

Deuteronomy 22:1 it'd be great if you could not see thy brother's ox or his sheep go astray, and hide thyself from them: it'd be great if you could in any case bring them again unto thy brother.

Deuteronomy 22:2 and if thy brother be not nigh unto thee, or if thou know him not, then it'd be great if you could bring it unto thine own house, and it shall be with thee until thy brother seek after it, and it'd be great if you could restore it to him again.

Deuteronomy 22:4 it'd be great if you could not see thy brother's ass or his ox fall down by the way, and hide thyself from them: it'd be great if you could surely help him to lift them up again.

Deuteronomy 22:6 if a bird's nest chance to be before thee in the way in any tree, or on the ground, whether they be young ones, or eggs, and the dam sitting upon the young, or upon the eggs, it'd be great if you could not take the dam with the young:

Deuteronomy 22:7 but it'd be great if you could in any wise let the dam go, and take the young to thee; that it may be well with thee, and that thou mayest prolong thy days.

Deuteronomy 22:8 when thou buildest a new house, then it'd be great if you could make a battlement for thy roof, that thou bring not blood upon thine house, if any man fall from thence.

Deuteronomy 22:9 it'd be great if you could not sow thy vineyard with divers seeds: lest the fruit of thy seed which thou hast sown, and the fruit of thy vineyard, be defiled.

Deuteronomy 22:10 it'd be great if you could not plow with an ox and an ass together.

Deuteronomy 22:11 it'd be great if you could not wear a garment of divers sorts, as of woollen and linen together.

Deuteronomy 22:12 it'd be great if you could make thee fringes upon the four quarters of thy vesture, wherewith thou coverest thyself.

Deuteronomy 22:24 then ye shall bring them both out unto the gate of that city, and ye shall stone them with stones that they die; the damsel, because she cried not, being in the city; and the man, because he hath humbled his neighbour's wife: so it'd be great if you could put away evil from among you.

Deuteronomy 22:26 but unto the damsel it'd be great if you could do nothing; there is in the damsel no sin worthy of death: for as when a man riseth against his neighbour, and slayeth him, even so is this matter:

Deuteronomy 23:6 it'd be great if you could not seek their peace nor their prosperity all thy days for ever.

Deuteronomy 23:7 it'd be great if you could not abhor an edomite; for he is thy brother: it'd be great if you could not abhor an egyptian; because thou wast a stranger in his land.

Deuteronomy 23:12 it'd be great if you could have a place also without the camp, whither it'd be great if you could go forth abroad:

Deuteronomy 23:13 and it'd be great if you could have a paddle upon thy weapon; and it shall be, when thou wilt ease thyself abroad, it'd be great if you could dig therewith, and shalt turn back and cover that which cometh from thee:

Deuteronomy 23:15 it'd be great if you could not deliver unto his master the servant which is escaped from his master unto thee:

Deuteronomy 23:16 he shall dwell with thee, even among you, in that place which he shall choose in one of thy gates, where it liketh him best: it'd be great if you could not oppress him.

Deuteronomy 23:18 it'd be great if you could not bring the hire of a whore, or the price of a dog, into the house of the lord thy god for any vow: for even both these are abomination unto the lord thy god.

Deuteronomy 23:19 it'd be great if you could not lend upon usury to thy brother; usury of money, usury of victuals, usury of any thing that is lent upon usury:

Deuteronomy 23:20 unto a stranger thou mayest lend upon usury; but unto thy brother it'd be great if you could not lend upon usury: that the lord thy god may bless thee in all that thou settest thine hand to in the land whither thou goest to possess it.

Deuteronomy 23:21 when it'd be great if you could vow a vow unto the lord thy god, it'd be great if you could not slack to pay it: for the lord thy god will surely require it of thee; and it would be sin in thee.

Deuteronomy 23:22 but if it'd be great if you could forbear to vow, it shall be no sin in thee.

Deuteronomy 23:23 that which is gone out of thy lips it'd be great if you could keep and perform; even a freewill offering, according as thou hast vowed unto the lord thy god, which thou hast promised with thy mouth.

Deuteronomy 23:24 when thou comest into thy neighbour's vineyard, then thou mayest eat grapes thy fill at thine own pleasure; but it'd be great if you could not put any in thy vessel.

Deuteronomy 23:25 when thou comest into the standing corn of thy neighbour, then thou mayest pluck the ears with thine hand; but it'd be great if you could not move a sickle unto thy neighbour's standing corn.

Deuteronomy 24:4 her former husband, which sent her away, may not take her again to be his wife, after that she is defiled; for that is abomination before the lord: and it'd be great if you could not cause the land to sin, which the lord thy god giveth thee for an inheritance.

Deuteronomy 24:7 if a man be found stealing any of his brethren of the children of israel, and maketh merchandise of him, or selleth him; then that thief shall die; and it'd be great if you could put evil away from among you.

Deuteronomy 24:10 when thou dost lend thy brother any thing, it'd be great if you could not go into his house to fetch his pledge.

Deuteronomy 24:11 it'd be great if you could stand abroad, and the man to whom thou dost lend shall bring out the pledge abroad unto thee.

Deuteronomy 24:12 and if the man be poor, it'd be great if you could not sleep with his pledge:

Deuteronomy 24:13 in any case it'd be great if you could deliver him the pledge again when the sun goeth down, that he may sleep in his own raiment, and bless thee: and it shall be righteousness unto thee before the lord thy god.

Deuteronomy 24:14 it'd be great if you could not oppress an hired servant that is poor and needy, whether he be of thy brethren, or of thy strangers that are in thy land within thy gates:

Deuteronomy 24:15 at his day it'd be great if you could give him his hire, neither shall the sun go down upon it; for he is poor, and setteth his heart upon it: lest he cry against thee unto the lord, and it be sin unto thee.

Deuteronomy 24:17 it'd be great if you could not pervert the judgment of the stranger, nor of the fatherless; nor take a widow's raiment to pledge:

Deuteronomy 24:18 but it'd be great if you could remember that thou wast a bondman in egypt, and the lord thy god redeemed thee thence: therefore i command thee to do this thing.

Deuteronomy 24:19 when thou cuttest down thine harvest in thy field, and hast forgot a sheaf in the field, it'd be great if you could not go again to fetch it: it shall be for the stranger, for the fatherless, and for the widow: that the lord thy god may bless thee in all the work of thine hands.

Deuteronomy 24:20 when thou beatest thine olive tree, it'd be great if you could not go over the boughs again: it shall be for the stranger, for the fatherless, and for the widow.

Deuteronomy 24:21 when thou gatherest the grapes of thy vineyard, it'd be great if you could not glean it afterward: it shall be for the stranger, for the fatherless, and for the widow.

Deuteronomy 24:22 and it'd be great if you could remember that thou wast a bondman in the land of egypt: therefore i command thee to do this thing.

Deuteronomy 25:4 it'd be great if you could not muzzle the ox when he treadeth out the corn.

Deuteronomy 25:12 then it'd be great if you could cut off her hand, thine eye shall not pity her.

Deuteronomy 25:13 it'd be great if you could not have in thy bag divers weights, a great and a small.

Deuteronomy 25:14 it'd be great if you could not have in thine house divers measures, a great and a small.

Deuteronomy 25:15 but it'd be great if you could have a perfect and just weight, a perfect and just measure shalt thou have: that thy days may be lengthened in the land which the lord thy god giveth thee.

Deuteronomy 25:19 therefore it shall be, when the lord thy god hath given thee rest from all thine enemies round about, in the land which the lord thy god giveth thee for an inheritance to possess it, that it'd be great if you could blot out the remembrance of amalek from under heaven; it'd be great if you could not forget it.

Deuteronomy 26:2 that it'd be great if you could take of the first of all the fruit of the earth, which it'd be great if you could bring of thy land that the lord thy god giveth thee, and shalt put it in a basket, and shalt go unto the place which the lord thy god shall choose to place his name there.

Deuteronomy 26:3 and it'd be great if you could go unto the priest that shall be in those days, and say unto him, i profess this day unto the lord thy god, that i am come unto the country which the lord sware unto our fathers for to give us.

Deuteronomy 26:5 and it'd be great if you could speak and say before the lord thy god, a syrian ready to perish was my father, and he went down into egypt, and sojourned there with a few, and became there a nation, great, mighty, and populous:

Deuteronomy 26:10 and now, behold, i have brought the firstfruits of the land, which thou, o lord, hast given me. and it'd be great if you could set it before the lord thy god, and worship before the lord thy god:

Deuteronomy 26:11 and it'd be great if you could rejoice in every good thing which the lord thy god hath given unto thee, and unto thine house, thou, and the levite, and the stranger that is among you.

Deuteronomy 26:13 then it'd be great if you could say before the lord thy god, i have brought away the hallowed things out of mine house, and also have given them unto the levite, and unto the stranger, to the fatherless, and to the widow, according to all thy commandments which thou hast commanded me: i have not transgressed thy commandments, neither have i forgotten them:

Deuteronomy 26:16 this day the lord thy god hath commanded thee to do these statutes and judgments: it'd be great if you could therefore keep and do them with all thine heart, and with all thy soul.

Deuteronomy 27:2 and it shall be on the day when ye shall pass over jordan unto the land which the lord thy god giveth thee, that it'd be great if you could set thee up great stones, and plaister them with plaister:

Deuteronomy 27:3 and it'd be great if you could write upon them all the words of this law, when thou art passed over, that thou mayest go in unto the land which the lord thy god giveth thee, a land that floweth with milk and honey; as the lord god of thy fathers hath promised thee.

Deuteronomy 27:4 therefore it shall be when ye be gone over jordan, that ye shall set up these stones, which i command you this day, in mount ebal, and it'd be great if you could plaister them with plaister.

Deuteronomy 27:5 and there shalt thou build an altar unto the lord thy god, an altar of stones: it'd be great if you could not lift up any iron tool upon them.

Deuteronomy 27:6 it'd be great if you could build the altar of the lord thy god of whole stones: and it'd be great if you could offer burnt offerings thereon unto the lord thy god:

Deuteronomy 27:7 and it'd be great if you could offer peace offerings, and shalt eat there, and rejoice before the lord thy god.
 
  Deuteronomy 27:8 and it'd be great if you could write upon the stones all the words of this law very plainly.

Deuteronomy 27:10 it'd be great if you could therefore obey the voice of the lord thy god, and do his commandments and his statutes, which i command thee this day.

Deuteronomy 28:1 and it shall come to pass, if it'd be great if you could hearken diligently unto the voice of the lord thy god, to observe and to do all his commandments which i command thee this day, that the lord thy god will set thee on high above all nations of the earth:

Deuteronomy 28:2 and all these blessings shall come on thee, and overtake thee, if it'd be great if you could hearken unto the voice of the lord thy god.

Deuteronomy 28:9 the lord shall establish thee an holy people unto himself, as he hath sworn unto thee, if it'd be great if you could keep the commandments of the lord thy god, and walk in his ways.

Deuteronomy 28:12 the lord shall open unto thee his good treasure, the heaven to give the rain unto thy land in his season, and to bless all the work of thine hand: and it'd be great if you could lend unto many nations, and it'd be great if you could not borrow.

Deuteronomy 28:13 and the lord shall make thee the head, and not the tail; and it'd be great if you could be above only, and it'd be great if you could not be beneath; if that thou hearken unto the commandments of the lord thy god, which i command thee this day, to observe and to do them:

Deuteronomy 28:14 and it'd be great if you could not go aside from any of the words which i command thee this day, to the right hand, or to the left, to go after other gods to serve them.

Deuteronomy 28:25 the lord shall cause thee to be smitten before thine enemies: it'd be great if you could go out one way against them, and flee seven ways before them: and shalt be removed into all the kingdoms of the earth.

Deuteronomy 28:29 and it'd be great if you could grope at noonday, as the blind gropeth in darkness, and it'd be great if you could not prosper in thy ways: and it'd be great if you could be only oppressed and spoiled evermore, and no man shall save thee.

Deuteronomy 28:30 it'd be great if you could betroth a wife, and another man shall lie with her: it'd be great if you could build an house, and it'd be great if you could not dwell therein: it'd be great if you could plant a vineyard, and shalt not gather the grapes thereof.

Deuteronomy 28:31 thine ox shall be slain before thine eyes, and it'd be great if you could not eat thereof: thine ass shall be violently taken away from before thy face, and shall not be restored to thee: thy sheep shall be given unto thine enemies, and it'd be great if you could have none to rescue them.

Deuteronomy 28:33 the fruit of thy land, and all thy labours, shall a nation which thou knowest not eat up; and it'd be great if you could be only oppressed and crushed alway:

Deuteronomy 28:34 so that it'd be great if you could be mad for the sight of thine eyes which it'd be great if you could see.

Deuteronomy 28:36 the lord shall bring thee, and thy king which it'd be great if you could set over thee, unto a nation which neither thou nor thy fathers have known; and there shalt thou serve other gods, wood and stone.

Deuteronomy 28:37 and it'd be great if you could become an astonishment, a proverb, and a byword, among all nations whither the lord shall lead thee.

Deuteronomy 28:38 it'd be great if you could carry much seed out into the field, and shalt gather but little in; for the locust shall consume it.

Deuteronomy 28:39 it'd be great if you could plant vineyards, and dress them, but shalt neither drink of the wine, nor gather the grapes; for the worms shall eat them.

Deuteronomy 28:40 it'd be great if you could have olive trees throughout all thy coasts, but it'd be great if you could not anoint thyself with the oil; for thine olive shall cast his fruit.

Deuteronomy 28:41 it'd be great if you could beget sons and daughters, but it'd be great if you could not enjoy them; for they shall go into captivity.

Deuteronomy 28:43 the stranger that is within thee shall get up above thee very high; and it'd be great if you could come down very low.

Deuteronomy 28:44 he shall lend to thee, and it'd be great if you could not lend to him: he shall be the head, and it'd be great if you could be the tail.

Deuteronomy 28:49 the lord shall bring a nation against thee from far, from the end of the earth, as swift as the eagle flieth; a nation whose tongue it'd be great if you could not understand;

Deuteronomy 28:53 and it'd be great if you could eat the fruit of thine own body, the flesh of thy sons and of thy daughters, which the lord thy god hath given thee, in the siege, and in the straitness, wherewith thine enemies shall distress thee:

Deuteronomy 28:64 and the lord shall scatter thee among all people, from the one end of the earth even unto the other; and there it'd be great if you could serve other gods, which neither thou nor thy fathers have known, even wood and stone.

Deuteronomy 28:66 and thy life shall hang in doubt before thee; and it'd be great if you could fear day and night, and shalt have none assurance of thy life:

Deuteronomy 28:67 in the morning it'd be great if you could say, would god it were even! and at even it'd be great if you could say, would god it were morning! for the fear of thine heart wherewith it'd be great if you could fear, and for the sight of thine eyes which it'd be great if you could see.

Deuteronomy 28:68 and the lord shall bring thee into egypt again with ships, by the way whereof i spake unto thee, it'd be great if you could see it no more again: and there ye shall be sold unto your enemies for bondmen and bondwomen, and no man shall buy you.

Deuteronomy 30:1 and it shall come to pass, when all these things are come upon thee, the blessing and the curse, which i have set before thee, and it'd be great if you could call them to mind among all the nations, whither the lord thy god hath driven thee,

Deuteronomy 30:5 and the lord thy god will bring thee into the land which thy fathers possessed, and it'd be great if you could possess it; and he will do thee good, and multiply thee above thy fathers.

Deuteronomy 30:8 and it'd be great if you could return and obey the voice of the lord, and do all his commandments which i command thee this day.

Deuteronomy 30:10 if it'd be great if you could hearken unto the voice of the lord thy god, to keep his commandments and his statutes which are written in this book of the law, and if thou turn unto the lord thy god with all thine heart, and with all thy soul.

Deuteronomy 31:2 and he said unto them, i am an hundred and twenty years old this day; i can no more go out and come in: also the lord hath said unto me, it'd be great if you could not go over this jordan.

Deuteronomy 31:3 the lord thy god, he will go over before thee, and he will destroy these nations from before thee, and it'd be great if you could possess them: and joshua, he shall go over before thee, as the lord hath said.

Deuteronomy 31:7 and moses called unto joshua, and said unto him in the sight of all israel, be strong and of a good courage: for thou must go with this people unto the land which the lord hath sworn unto their fathers to give them; and it'd be great if you could cause them to inherit it.

Deuteronomy 31:11 when all israel is come to appear before the lord thy god in the place which he shall choose, it'd be great if you could read this law before all israel in their hearing.

Deuteronomy 31:16 and the lord said unto moses, behold, it'd be great if you could sleep with thy fathers; and this people will rise up, and go a whoring after the gods of the strangers of the land, whither they go to be among them, and will forsake me, and break my covenant which i have made with them.

Deuteronomy 31:23 and he gave joshua the son of nun a charge, and said, be strong and of a good courage: for it'd be great if you could bring the children of israel into the land which i sware unto them: and i will be with thee.

Deuteronomy 32:52 yet it'd be great if you could see the land before thee; but it'd be great if you could not go thither unto the land which i give the children of israel.

Deuteronomy 33:29 happy art thou, o israel: who is like unto thee, o people saved by the lord, the shield of thy help, and who is the sword of thy excellency! and thine enemies shall be found liars unto thee; and it'd be great if you could tread upon their high places.

Deuteronomy 34:4 and the lord said unto him, this is the land which i sware unto abraham, unto isaac, and unto jacob, saying, i will give it unto thy seed: i have caused thee to see it with thine eyes, but it'd be great if you could not go over thither.

Joshua 1:8 this book of the law shall not depart out of thy mouth; but it'd be great if you could meditate therein day and night, that thou mayest observe to do according to all that is written therein: for then it'd be great if you could make thy way prosperous, and then it'd be great if you could have good success.

Joshua 2:18 behold, when we come into the land, it'd be great if you could bind this line of scarlet thread in the window which thou didst let us down by: and it'd be great if you could bring thy father, and thy mother, and thy brethren, and all thy father's household, home unto thee.

Joshua 3:8 and it'd be great if you could command the priests that bear the ark of the covenant, saying, when ye are come to the brink of the water of jordan, ye shall stand still in jordan.

Joshua 8:2 and it'd be great if you could do to ai and her king as thou didst unto jericho and her king: only the spoil thereof, and the cattle thereof, shall ye take for a prey unto yourselves: lay thee an ambush for the city behind it.

Joshua 11:6 and the lord said unto joshua, be not afraid because of them: for to morrow about this time will i deliver them up all slain before israel: it'd be great if you could hough their horses, and burn their chariots with fire.

Joshua 17:17 and joshua spake unto the house of joseph, even to ephraim and to manasseh, saying, thou art a great people, and hast great power: it'd be great if you could not have one lot only:

Joshua 17:18 but the mountain shall be thine; for it is a wood, and it'd be great if you could cut it down: and the outgoings of it shall be thine: for it'd be great if you could drive out the canaanites, though they have iron chariots, and though they be strong.

Judges 4:20 again he said unto her, stand in the door of the tent, and it shall be, when any man doth come and inquire of thee, and say, is there any man here? that it'd be great if you could say, no.

Judges 6:14 and the lord looked upon him, and said, go in this thy might, and it'd be great if you could save israel from the hand of the midianites: have not i sent thee?

Judges 6:16 and the lord said unto him, surely i will be with thee, and it'd be great if you could smite the midianites as one man.

Judges 6:23 and the lord said unto him, peace be unto thee; fear not: it'd be great if you could not die.

Judges 6:26 and build an altar unto the lord thy god upon the top of this rock, in the ordered place, and take the second bullock, and offer a burnt sacrifice with the wood of the grove which it'd be great if you could cut down.

Judges 7:11 and it'd be great if you could hear what they say; and afterward shall thine hands be strengthened to go down unto the host. then went he down with phurah his servant unto the outside of the armed men that were in the host.

Judges 9:33 and it shall be, that in the morning, as soon as the sun is up, it'd be great if you could rise early, and set upon the city: and, behold, when he and the people that is with him come out against thee, then mayest thou do to them as it'd be great if you could find occasion.

Judges 11:2 and gilead's wife bare him sons; and his wife's sons grew up, and they thrust out jephthah, and said unto him, it'd be great if you could not inherit in our father's house; for thou art the son of a strange woman.

Judges 11:30 and jephthah vowed a vow unto the lord, and said, if it'd be great if you could without fail deliver the children of ammon into mine hands,

Judges 13:3 and the angel of the lord appeared unto the woman, and said unto her, behold now, thou art barren, and bearest not: but it'd be great if you could conceive, and bear a son.

Judges 13:5 for, lo, it'd be great if you could conceive, and bear a son; and no razor shall come on his head: for the child shall be a nazarite unto god from the womb: and he shall begin to deliver israel out of the hand of the philistines.

Judges 13:7 but he said unto me, behold, it'd be great if you could conceive, and bear a son; and now drink no wine nor strong drink, neither eat any unclean thing: for the child shall be a nazarite to god from the womb to the day of his death.

Ruth 2:21 and ruth the moabitess said, he said unto me also, it'd be great if you could keep fast by my young men, until they have ended all my harvest.

Ruth 3:4 and it shall be, when he lieth down, that it'd be great if you could mark the place where he shall lie, and it'd be great if you could go in, and uncover his feet, and lay thee down; and he will tell thee what it'd be great if you could do.

1 Samuel 2:16 and if any man said unto him, let them not fail to burn the fat presently, and then take as much as thy soul desireth; then he would answer him, nay; but it'd be great if you could give it me now: and if not, i will take it by force.

1 Samuel 2:32 and it'd be great if you could see an enemy in my habitation, in all the wealth which god shall give israel: and there shall not be an old man in thine house for ever.

1 Samuel 3:9 therefore eli said unto samuel, go, lie down: and it shall be, if he call thee, that it'd be great if you could say, speak, lord; for thy servant heareth. so samuel went and lay down in his place.

1 Samuel 9:16 to morrow about this time i will send thee a man out of the land of benjamin, and it'd be great if you could anoint him to be captain over my people israel, that he may save my people out of the hand of the philistines: for i have looked upon my people, because their cry is come unto me.

1 Samuel 10:2 when thou art departed from me to day, then it'd be great if you could find two men by rachel's sepulchre in the border of benjamin at zelzah; and they will say unto thee, the asses which thou wentest to seek are found: and, lo, thy father hath left the care of the asses, and sorroweth for you, saying, what shall i do for my son?

1 Samuel 10:3 then shalt thou go on forward from thence, and it'd be great if you could come to the plain of tabor, and there shall meet thee three men going up to god to beth-el, one carrying three kids, and another carrying three loaves of bread, and another carrying a bottle of wine:

1 Samuel 10:4 and they will salute thee, and give thee two loaves of bread; which it'd be great if you could receive of their hands.

1 Samuel 10:5 after that it'd be great if you could come to the hill of god, where is the garrison of the philistines: and it shall come to pass, when thou art come thither to the city, that it'd be great if you could meet a company of prophets coming down from the high place with a psaltery, and a tabret, and a pipe, and a harp, before them; and they shall prophesy:

1 Samuel 10:6 and the spirit of the lord will come upon thee, and it'd be great if you could prophesy with them, and shalt be turned into another man.

1 Samuel 10:8 and it'd be great if you could go down before me to gilgal; and, behold, i will come down unto thee, to offer burnt offerings, and to sacrifice sacrifices of peace offerings: seven days shalt thou tarry, till i come to thee, and shew thee what it'd be great if you could do.

1 Samuel 14:44 and saul answered, god do so and more also: for it'd be great if you could surely die, jonathan.

1 Samuel 16:3 and call jesse to the sacrifice, and i will shew thee what it'd be great if you could do: and it'd be great if you could anoint unto me him whom i name unto thee.

1 Samuel 16:16 let our lord now command thy servants, which are before thee, to seek out a man, who is a cunning player on an harp: and it shall come to pass, when the evil spirit from god is upon thee, that he shall play with his hand, and it'd be great if you could be well.

1 Samuel 18:21 and saul said, i will give him her, that she may be a snare to him, and that the hand of the philistines may be against him. wherefore saul said to david, it'd be great if you could this day be my son in law in the one of the twain.

1 Samuel 19:11 saul also sent messengers unto david's house, to watch him, and to slay him in the morning: and michal david's wife told him, saying, if thou save not thy life to night, to morrow it'd be great if you could be slain.

1 Samuel 20:2 and he said unto him, god forbid; it'd be great if you could not die: behold, my father will do nothing either great or small, but that he will shew it me: and why should my father hide this thing from me? it is not so.

1 Samuel 20:8 therefore it'd be great if you could deal kindly with thy servant; for thou hast brought thy servant into a covenant of the lord with thee: notwithstanding, if there be in me iniquity, slay me thyself; for why shouldest thou bring me to thy father?

1 Samuel 20:14 and it'd be great if you could not only while yet i live shew me the kindness of the lord, that i die not:

1 Samuel 20:15 but also it'd be great if you could not cut off thy kindness from my house for ever: no, not when the lord hath cut off the enemies of david every one from the face of the earth.

1 Samuel 20:18 then jonathan said to david, to morrow is the new moon: and it'd be great if you could be missed, because thy seat will be empty.

1 Samuel 20:19 and when thou hast stayed three days, then it'd be great if you could go down quickly, and come to the place where thou didst hide thyself when the business was in hand, and shalt remain by the stone ezel.

1 Samuel 20:31 for as long as the son of jesse liveth upon the ground, it'd be great if you could not be established, nor thy kingdom. wherefore now send and fetch him unto me, for he shall surely die.

1 Samuel 22:16 and the king said, it'd be great if you could surely die, ahimelech, thou, and all thy father's house.

1 Samuel 22:23 abide thou with me, fear not: for he that seeketh my life seeketh thy life: but with me it'd be great if you could be in safeguard.

1 Samuel 23:17 and he said unto him, fear not: for the hand of saul my father shall not find thee; and it'd be great if you could be king over israel, and i shall be next unto thee; and that also saul my father knoweth.

1 Samuel 24:20 and now, behold, i know well that it'd be great if you could surely be king, and that the kingdom of israel shall be established in thine hand.

1 Samuel 26:25 then saul said to david, blessed be thou, my son david: it'd be great if you could both do great things, and also shalt still prevail. so david went on his way, and saul returned to his place.

1 Samuel 28:1 and it came to pass in those days, that the philistines gathered their armies together for warfare, to fight with israel. and achish said unto david, know thou assuredly, that it'd be great if you could go out with me to battle, thou and thy men.

1 Samuel 28:2 and david said to achish, surely it'd be great if you could know what thy servant can do. and achish said to david, therefore will i make thee keeper of mine head for ever.

1 Samuel 30:8 and david inquired at the lord, saying, shall i pursue after this troop? shall i overtake them? and he answered him, pursue: for it'd be great if you could surely overtake them, and without fail recover all.

2 Samuel 3:13 and he said, well; i will make a league with thee: but one thing i require of thee, that is, it'd be great if you could not see my face, except thou first bring michal saul's daughter, when thou comest to see my face.

2 Samuel 5:2 also in time past, when saul was king over us, thou wast he that leddest out and broughtest in israel: and the lord said to thee, it'd be great if you could feed my people israel, and it'd be great if you could be a captain over israel.

2 Samuel 5:6 and the king and his men went to jerusalem unto the jebusites, the inhabitants of the land: which spake unto david, saying, except thou take away the blind and the lame, it'd be great if you could not come in hither: thinking, david cannot come in hither.

2 Samuel 5:23 and when david enquired of the lord, he said, it'd be great if you could not go up; but fetch a compass behind them, and come upon them over against the mulberry trees.

2 Samuel 5:24 and let it be, when thou hearest the sound of a going in the tops of the mulberry trees, that then it'd be great if you could bestir thyself: for then shall the lord go out before thee, to smite the host of the philistines.

2 Samuel 7:12 and when thy days be fulfilled, and it'd be great if you could sleep with thy fathers, i will set up thy seed after thee, which shall proceed out of thy bowels, and i will establish his kingdom.

2 Samuel 9:7 and david said unto him, fear not: for i will surely shew thee kindness for jonathan thy father's sake, and will restore thee all the land of saul thy father; and it'd be great if you could eat bread at my table continually.

2 Samuel 9:10 thou therefore, and thy sons, and thy servants, shall till the land for him, and it'd be great if you could bring in the fruits, that thy master's son may have food to eat: but mephibosheth thy master's son shall eat bread alway at my table. now ziba had fifteen sons and twenty servants.

2 Samuel 10:11 and he said, if the syrians be too strong for me, then it'd be great if you could help me: but if the children of ammon be too strong for thee, then i will come and help thee.

2 Samuel 12:13 and david said unto nathan, i have sinned against the lord. and nathan said unto david, the lord also hath put away thy sin; it'd be great if you could not die.

2 Samuel 13:13 and i, whither shall i cause my shame to go? and as for thee, it'd be great if you could be as one of the fools in israel. now therefore, i pray thee, speak unto the king; for he will not withhold me from thee.

2 Samuel 15:33 unto whom david said, if thou passest on with me, then it'd be great if you could be a burden unto me:

2 Samuel 15:35 and hast thou not there with thee zadok and abiathar the priests? therefore it shall be, that what thing soever it'd be great if you could hear out of the king's house, it'd be great if you could tell it to zadok and abiathar the priests.

2 Samuel 18:3 but the people answered, it'd be great if you could not go forth: for if we flee away, they will not care for us; neither if half of us die, will they care for us: but now thou art worth ten thousand of us: therefore now it is better that thou succour us out of the city.

2 Samuel 18:20 and joab said unto him, it'd be great if you could not bear tidings this day, but it'd be great if you could bear tidings another day: but this day it'd be great if you could bear no tidings, because the king's son is dead.

2 Samuel 19:23 therefore the king said unto shimei, it'd be great if you could not die. and the king sware unto him.

2 Samuel 19:38 and the king answered, chimham shall go over with me, and i will do to him that which shall seem good unto thee: and whatsoever it'd be great if you could require of me, that will i do for thee.

2 Samuel 21:17 but abishai the son of zeruiah succoured him, and smote the philistine, and killed him. then the men of david sware unto him, saying, it'd be great if you could go no more out with us to battle, that thou quench not the light of israel.

1 Kings 2:37 for it shall be, that on the day thou goest out, and passest over the brook kidron, it'd be great if you could know for certain that it'd be great if you could surely die: thy blood shall be upon thine own head.

1 Kings 2:42 and the king sent and called for shimei, and said unto him, did i not make thee to swear by the lord, and protested unto thee, saying, know for a certain, on the day thou goest out, and walkest abroad any wither, that it'd be great if you could surely die? and thou saidst unto me, the word that i have heard is good.

1 Kings 5:6 now therefore command thou that they hew me cedar trees out of lebanon; and my servants shall be with thy servants: and unto thee will i give hire for thy servants according to all that it'd be great if you could appoint: for thou knowest that there is not among us any that can skill to hew timber like unto the sidonians.

1 Kings 5:9 my servants shall bring them down from lebanon unto the sea: and i will convey them by sea in floats unto the place that it'd be great if you could appoint me, and will cause them to be discharged there, and it'd be great if you could receive them: and it'd be great if you could accomplish my desire, in giving food for my household.

1 Kings 8:19 nevertheless it'd be great if you could not build the house; but thy son that shall come forth out of thy loins, he shall build the house unto my name.

1 Kings 8:44 if thy people go out to battle against their enemy, whithersoever it'd be great if you could send them, and shall pray unto the lord toward the city which thou hast chosen, and toward the house that i have built for thy name:

1 Kings 11:37 and i will take thee, and it'd be great if you could reign according to all that thy soul desireth, and shalt be king over israel.

1 Kings 13:17 for it was said to me by the word of the lord, it'd be great if you could eat no bread nor drink water there, nor turn again to go by the way that thou camest.

1 Kings 17:4 and it shall be, that it'd be great if you could drink of the brook; and i have commanded the ravens to feed thee there.

1 Kings 20:5 and the messengers came again, and said, thus speaketh ben-hadad, saying, although i have sent unto thee, saying, it'd be great if you could deliver me thy silver, and thy gold, and thy wives, and thy children;

1 Kings 20:13 and, behold, there came a prophet unto ahab king of israel, saying, thus saith the lord, hast thou seen all this great multitude? behold, i will deliver it into thine hand this day; and it'd be great if you could know that i am the lord.

1 Kings 20:34 and ben-hadad said unto him, the cities, which my father took from thy father, i will restore; and it'd be great if you could make streets for thee in damascus, as my father made in samaria. then said ahab, i will send thee away with this covenant. so he made a covenant with him, and sent him away.

1 Kings 20:39 and as the king passed by, he cried unto the king: and he said, thy servant went out into the midst of the battle; and, behold, a man turned aside, and brought a man unto me, and said, keep this man: if by any means he be missing, then shall thy life be for his life, or else it'd be great if you could pay a talent of silver.

1 Kings 21:19 and it'd be great if you could speak unto him, saying, thus saith the lord, hast thou killed, and also taken possession? and it'd be great if you could speak unto him, saying, thus saith the lord, in the place where dogs licked the blood of naboth shall dogs lick thy blood, even thine.

1 Kings 22:22 and the lord said unto him, wherewith? and he said, i will go forth, and i will be a lying spirit in the mouth of all his prophets. and he said, it'd be great if you could persuade him, and prevail also: go forth, and do so.

1 Kings 22:25 and micaiah said, behold, it'd be great if you could see in that day, when it'd be great if you could go into an inner chamber to hide thyself.

2 Kings 1:4 now therefore thus saith the lord, it'd be great if you could not come down from that bed on which thou art gone up, but shalt surely die. and elijah departed.

2 Kings 1:6 and they said unto him, there came a man up to meet us, and said unto us, go, turn again unto the king that sent you, and say unto him, thus saith the lord, is it not because there is not a god in israel, that thou sendest to enquire of baal-zebub the god of ekron? therefore it'd be great if you could not come down from that bed on which thou art gone up, but shalt surely die.

2 Kings 1:16 and he said unto him, thus saith the lord, forasmuch as thou hast sent messengers to enquire of baal-zebub the god of ekron, is it not because there is no god in israel to enquire of his word? therefore it'd be great if you could not come down off that bed on which thou art gone up, but shalt surely die.

2 Kings 4:4 and when thou art come in, it'd be great if you could shut the door upon thee and upon thy sons, and shalt pour out into all those vessels, and it'd be great if you could set aside that which is full.

2 Kings 4:16 and he said, about this season, according to the time of life, it'd be great if you could embrace a son. and she said, nay, my lord, thou man of god, do not lie unto thine handmaid.

2 Kings 5:10 and elisha sent a messenger unto him, saying, go and wash in jordan seven times, and thy flesh shall come again to thee, and it'd be great if you could be clean.

2 Kings 6:22 and he answered, it'd be great if you could not smite them: wouldest thou smite those whom thou hast taken captive with thy sword and with thy bow? set bread and water before them, that they may eat and drink, and go to their master.

2 Kings 7:2 then a lord on whose hand the king leaned answered the man of god, and said, behold, if the lord would make windows in heaven, might this thing be? and he said, behold, it'd be great if you could see it with thine eyes, but shalt not eat thereof.

2 Kings 7:19 and that lord answered the man of god, and said, now, behold, if the lord should make windows in heaven, might such a thing be? and he said, behold, it'd be great if you could see it with thine eyes, but shalt not eat thereof.

2 Kings 8:13 and hazael said, but what, is thy servant a dog, that he should do this great thing? and elisha answered, the lord hath shewed me that it'd be great if you could be king over syria.

2 Kings 9:7 and it'd be great if you could smite the house of ahab thy master, that i may avenge the blood of my servants the prophets, and the blood of all the servants of the lord, at the hand of jezebel.

2 Kings 10:5 and he that was over the house, and he that was over the city, the elders also, and the bringers up of the children, sent to jehu, saying, we are thy servants, and will do all that it'd be great if you could bid us; we will not make any king: do thou that which is good in thine eyes.

2 Kings 13:17 and he said, open the window eastward. and he opened it. then elisha said, shoot. and he shot. and he said, the arrow of the lord's deliverance, and the arrow of deliverance from syria: for it'd be great if you could smite the syrians in aphek, till thou have consumed them.

2 Kings 13:19 and the man of god was wroth with him, and said, thou shouldest have smitten five or six times; then hadst thou smitten syria till thou hadst consumed it: whereas now it'd be great if you could smite syria but thrice.

2 Kings 20:1 in those days was hezekiah sick unto death. and the prophet isaiah the son of amoz came to him, and said unto him, thus saith the lord, set thine house in order; for it'd be great if you could die, and not live.

2 Kings 20:5 turn again, and tell hezekiah the captain of my people, thus saith the lord, the god of david thy father, i have heard thy prayer, i have seen thy tears: behold, i will heal thee: on the third day it'd be great if you could go up unto the house of the lord.

2 Kings 20:18 and of thy sons that shall issue from thee, which it'd be great if you could beget, shall they take away; and they shall be eunuchs in the palace of the king of babylon.

2 Kings 22:20 behold therefore, i will gather thee unto thy fathers, and it'd be great if you could be gathered into thy grave in peace; and thine eyes shall not see all the evil which i will bring upon this place. and they brought the king word again.

1 Chronicles 11:2 and moreover in time past, even when saul was king, thou wast he that leddest out and broughtest in israel: and the lord thy god said unto thee, it'd be great if you could feed my people israel, and it'd be great if you could be ruler over my people israel.

1 Chronicles 11:5 and the inhabitants of jebus said to david, it'd be great if you could not come hither. nevertheless david took the castle of zion, which is the city of david.

1 Chronicles 14:15 and it shall be, when it'd be great if you could hear a sound of going in the tops of the mulberry trees, that then it'd be great if you could go out to battle: for god is gone forth before thee to smite the host of the philistines.

1 Chronicles 17:4 go and tell david my servant, thus saith the lord, it'd be great if you could not build me an house to dwell in:

1 Chronicles 19:12 and he said, if the syrians be too strong for me, then it'd be great if you could help me: but if the children of ammon be too strong for thee, then i will help thee.

1 Chronicles 21:22 then david said to ornan, grant me the place of this threshingfloor, that i may build an altar therein unto the lord: it'd be great if you could grant it me for the full price: that the plague may be stayed from the people.

1 Chronicles 22:8 but the word of the lord came to me, saying, thou hast shed blood abundantly, and hast made great wars: it'd be great if you could not build an house unto my name, because thou hast shed much blood upon the earth in my sight.

1 Chronicles 28:3 but god said unto me, it'd be great if you could not build an house for my name, because thou hast been a man of war, and hast shed blood.

2 Chronicles 2:16 and we will cut wood out of lebanon, as much as it'd be great if you could need: and we will bring it to thee in floats by sea to joppa; and thou shall carry it up to jerusalem.

2 Chronicles 6:9 notwithstanding it'd be great if you could not build the house; but thy son which shall come forth out of thy loins, he shall build the house for my name.

2 Chronicles 6:34 if thy people go out to war against their enemies by the way that it'd be great if you could send them, and they pray unto thee toward this city which thou hast chosen, and the house which i have built for thy name;

2 Chronicles 16:9 for the eyes of the lord run to and fro throughout the whole earth, to shew himself strong in the behalf of them whose heart is perfect toward him. herein thou hast done foolishly: therefore from henceforth it'd be great if you could have wars.

2 Chronicles 18:10 and zedekiah the son of chenaanah had made him horns of iron, and said, thus saith the lord, with these it'd be great if you could push syria until they be consumed.

2 Chronicles 18:21 and he said, i will go out, and be a lying spirit in the mouth of all his prophets. and the lord said, it'd be great if you could entice him, and it'd be great if you could also prevail: go out, and do even so.

2 Chronicles 18:24 and micaiah said, behold, it'd be great if you could see on that day when it'd be great if you could go into an inner chamber to hide thyself.

2 Chronicles 21:15 and it'd be great if you could have great sickness by disease of thy bowels, until thy bowels fall out by reason of the sickness day by day.

2 Chronicles 34:28 behold, i will gather thee to thy fathers, and it'd be great if you could be gathered to thy grave in peace, neither shall thine eyes see all the evil that i will bring upon this place, and upon the inhabitants of the same. so they brought the king word again.

Ezra 4:13 be it known now unto the king, that, if this city be builded, and the walls set up again, then will they not pay toll, tribute, and custom, and so it'd be great if you could endamage the revenue of the kings.

Ezra 4:16 we certify the king that, if this city be builded again, and the walls thereof set up, by this means it'd be great if you could have no portion on this side the river.

Ezra 7:20 and whatsoever more shall be needful for the house of thy god, which it'd be great if you could have occasion to bestow, bestow it out of the king's treasure house.

Esther 4:13 then mordecai commanded to answer esther, think not with thyself that it'd be great if you could escape in the king's house, more than all the jews.

Esther 6:13 and haman told zeresh his wife and all his friends every thing that had befallen him. then said his wise men and zeresh his wife unto him, if mordecai be of the seed of the jews, before whom thou hast begun to fall, it'd be great if you could not prevail against him, but shalt surely fall before him.

Job 5:21 it'd be great if you could be hid from the scourge of the tongue: neither shalt thou be afraid of destruction when it cometh.

Job 5:22 at destruction and famine it'd be great if you could laugh: neither shalt thou be afraid of the beasts of the earth.

Job 5:23 for it'd be great if you could be in league with the stones of the field: and the beasts of the field shall be at peace with thee.

Job 5:24 and it'd be great if you could know that thy tabernacle shall be in peace; and it'd be great if you could visit thy habitation, and shalt not sin.

Job 5:25 it'd be great if you could know also that thy seed shall be great, and thine offspring as the grass of the earth.

Job 5:26 it'd be great if you could come to thy grave in a full age, like as a shock of corn cometh in in his season.

Job 7:21 and why dost thou not pardon my transgression, and take away mine iniquity? for now shall i sleep in the dust; and it'd be great if you could seek me in the morning, but i shall not be.

Job 11:15 for then shalt thou lift up thy face without spot; yea, it'd be great if you could be stedfast, and shalt not fear:

Job 11:16 because it'd be great if you could forget thy misery, and remember it as waters that pass away:

Job 11:17 and thine age shall be clearer than the noonday; it'd be great if you could shine forth, it'd be great if you could be as the morning.

Job 11:18 and it'd be great if you could be secure, because there is hope; yea, it'd be great if you could dig about thee, and it'd be great if you could take thy rest in safety.

Job 11:19 also it'd be great if you could lie down, and none shall make thee afraid; yea, many shall make suit unto thee.

Job 14:15 it'd be great if you could call, and i will answer thee: thou wilt have a desire to the work of thine hands.

Job 22:23 if thou return to the almighty, it'd be great if you could be built up, it'd be great if you could put away iniquity far from thy tabernacles.

Job 22:25 yea, the almighty shall be thy defence, and it'd be great if you could have plenty of silver.

Job 22:27 it'd be great if you could make thy prayer unto him, and he shall hear thee, and it'd be great if you could pay thy vows.

Job 22:28 it'd be great if you could also decree a thing, and it shall be established unto thee: and the light shall shine upon thy ways.

Job 22:29 when men are cast down, then it'd be great if you could say, there is lifting up; and he shall save the humble person.

Job 35:14 although thou sayest it'd be great if you could not see him, yet judgment is before him; therefore trust thou in him.

Psalms 2:9 it'd be great if you could break them with a rod of iron; it'd be great if you could dash them in pieces like a potter's vessel.

Psalms 5:6 it'd be great if you could destroy them that speak leasing: the lord will abhor the bloody and deceitful man.

Psalms 12:7 it'd be great if you could keep them, o lord, it'd be great if you could preserve them from this generation for ever.

Psalms 21:9 it'd be great if you could make them as a fiery oven in the time of thine anger: the lord shall swallow them up in his wrath, and the fire shall devour them.

Psalms 21:12 therefore shalt thou make them turn their back, when it'd be great if you could make ready thine arrows upon thy strings against the face of them.

Psalms 31:20 it'd be great if you could hide them in the secret of thy presence from the pride of man: it'd be great if you could keep them secretly in a pavilion from the strife of tongues.

Psalms 32:7 thou art my hiding place; it'd be great if you could preserve me from trouble; it'd be great if you could compass me about with songs of deliverance. selah.

Psalms 32:8 i will instruct thee and teach thee in the way which it'd be great if you could go: i will guide thee with mine eye.

Psalms 36:8 they shall be abundantly satisfied with the fatness of thy house; and it'd be great if you could make them drink of the river of thy pleasures.

Psalms 37:3 trust in the lord, and do good; so shalt thou dwell in the land, and verily it'd be great if you could be fed.

Psalms 37:10 for yet a little while, and the wicked shall not be: yea, it'd be great if you could diligently consider his place, and it shall not be.

Psalms 37:34 wait on the lord, and keep his way, and he shall exalt thee to inherit the land: when the wicked are cut off, it'd be great if you could see it.

Psalms 50:15 and call upon me in the day of trouble: i will deliver thee, and it'd be great if you could glorify me.

Psalms 51:6 behold, thou desirest truth in the inward parts: and in the hidden part it'd be great if you could make me to know wisdom.

Psalms 59:8 but thou, o lord, shalt laugh at them; it'd be great if you could have all the heathen in derision.

Psalms 65:3 iniquities prevail against me: as for our transgressions, it'd be great if you could purge them away.

Psalms 67:4 o let the nations be glad and sing for joy: for it'd be great if you could judge the people righteously, and govern the nations upon earth. selah.

Psalms 71:21 it'd be great if you could increase my greatness, and comfort me on every side.

Psalms 73:20 as a dream when one awaketh; so, o lord, when thou awakest, it'd be great if you could despise their image.

Psalms 73:24 it'd be great if you could guide me with thy counsel, and afterward receive me to glory.

Psalms 82:8 arise, o god, judge the earth: for it'd be great if you could inherit all nations.

Psalms 91:5 it'd be great if you could not be afraid for the terror by night; nor for the arrow that flieth by day;

Psalms 91:13 it'd be great if you could tread upon the lion and adder: the young lion and the dragon shalt thou trample under feet.

Psalms 102:13 it'd be great if you could arise, and have mercy upon zion: for the time to favour her, yea, the set time, is come.

Psalms 102:26 they shall perish, but it'd be great if you could endure: yea, all of them shall wax old like a garment; as a vesture shalt thou change them, and they shall be changed:

Psalms 119:32 i will run the way of thy commandments, when it'd be great if you could enlarge my heart.

Psalms 128:2 for it'd be great if you could eat the labour of thine hands: happy shalt thou be, and it shall be well with thee.

Psalms 128:5 the lord shall bless thee out of zion: and it'd be great if you could see the good of jerusalem all the days of thy life.

Psalms 128:6 yea, it'd be great if you could see thy children's children, and peace upon israel.

Psalms 138:7 though i walk in the midst of trouble, thou wilt revive me: it'd be great if you could stretch forth thine hand against the wrath of mine enemies, and thy right hand shall save me.

Psalms 142:7 bring my soul out of prison, that i may praise thy name: the righteous shall compass me about; for it'd be great if you could deal bountifully with me.

Proverbs 3:24 when thou liest down, it'd be great if you could not be afraid: yea, it'd be great if you could lie down, and thy sleep shall be sweet.

Proverbs 4:12 when thou goest, thy steps shall not be straitened; and when thou runnest, it'd be great if you could not stumble.

Proverbs 9:12 if thou be wise, it'd be great if you could be wise for thyself: but if thou scornest, thou alone shalt bear it.

Proverbs 20:13 love not sleep, lest thou come to poverty; open thine eyes, and it'd be great if you could be satisfied with bread.

Proverbs 22:24 make no friendship with an angry man; and with a furious man it'd be great if you could not go:

Proverbs 23:14 it'd be great if you could beat him with the rod, and shalt deliver his soul from hell.

Proverbs 23:34 yea, it'd be great if you could be as he that lieth down in the midst of the sea, or as he that lieth upon the top of a mast.

Proverbs 24:6 for by wise counsel it'd be great if you could make thy war: and in multitude of counsellors there is safety.

Proverbs 25:22 for it'd be great if you could heap coals of fire upon his head, and the lord shall reward thee.

Proverbs 27:27 and it'd be great if you could have goats' milk enough for thy food, for the food of thy household, and for the maintenance for thy maidens.

Ecclesiastes 11:1 cast thy bread upon the waters: for it'd be great if you could find it after many days.

Ecclesiastes 12:1 remember now thy creator in the days of thy youth, while the evil days come not, nor the years draw nigh, when it'd be great if you could say, i have no pleasure in them;

Isaiah 1:26 and i will restore thy judges as at the first, and thy counsellors as at the beginning: afterward it'd be great if you could be called, the city of righteousness, the faithful city.

Isaiah 12:1 and in that day it'd be great if you could say, o lord, i will praise thee: though thou wast angry with me, thine anger is turned away, and thou comfortedst me.

Isaiah 14:4 that it'd be great if you could take up this proverb against the king of babylon, and say, how hath the oppressor ceased! the golden city ceased!

Isaiah 14:15 yet it'd be great if you could be brought down to hell, to the sides of the pit.

Isaiah 14:20 it'd be great if you could not be joined with them in burial, because thou hast destroyed thy land, and slain thy people: the seed of evildoers shall never be renowned.

Isaiah 23:12 and he said, it'd be great if you could no more rejoice, o thou oppressed virgin, daughter of zidon: arise, pass over to chittim; there also shalt thou have no rest.

Isaiah 25:5 it'd be great if you could bring down the noise of strangers, as the heat in a dry place; even the heat with the shadow of a cloud: the branch of the terrible ones shall be brought low.

Isaiah 29:4 and it'd be great if you could be brought down, and shalt speak out of the ground, and thy speech shall be low out of the dust, and thy voice shall be, as of one that hath a familiar spirit, out of the ground, and thy speech shall whisper out of the dust.

Isaiah 29:6 it'd be great if you could be visited of the lord of hosts with thunder, and with earthquake, and great noise, with storm and tempest, and the flame of devouring fire.

Isaiah 30:19 for the people shall dwell in zion at jerusalem: it'd be great if you could weep no more: he will be very gracious unto thee at the voice of thy cry; when he shall hear it, he will answer thee.

Isaiah 30:22 ye shall defile also the covering of thy graven images of silver, and the ornament of thy molten images of gold: it'd be great if you could cast them away as a menstruous cloth; it'd be great if you could say unto it, get thee hence.

Isaiah 30:23 then shall he give the rain of thy seed, that it'd be great if you could sow the ground withal; and bread of the increase of the earth, and it shall be fat and plenteous: in that day shall thy cattle feed in large pastures.

Isaiah 33:1 woe to thee that spoilest, and thou wast not spoiled; and dealest treacherously, and they dealt not treacherously with thee! when it'd be great if you could cease to spoil, it'd be great if you could be spoiled; and when it'd be great if you could make an end to deal treacherously, they shall deal treacherously with thee.

Isaiah 33:19 it'd be great if you could not see a fierce people, a people of a deeper speech than thou canst perceive; of a stammering tongue, that thou canst not understand.

Isaiah 38:1 in those days was hezekiah sick unto death. and isaiah the prophet the son of amoz came unto him, and said unto him, thus saith the lord, set thine house in order: for it'd be great if you could die, and not live.

Isaiah 39:7 and of thy sons that shall issue from thee, which it'd be great if you could beget, shall they take away; and they shall be eunuchs in the palace of the king of babylon.

Isaiah 41:12 it'd be great if you could seek them, and shalt not find them, even them that contended with thee: they that war against thee shall be as nothing, and as a thing of nought.

Isaiah 41:15 behold, i will make thee a new sharp threshing instrument having teeth: it'd be great if you could thresh the mountains, and beat them small, and shalt make the hills as chaff.

Isaiah 41:16 it'd be great if you could fan them, and the wind shall carry them away, and the whirlwind shall scatter them: and it'd be great if you could rejoice in the lord, and shalt glory in the holy one of israel.

Isaiah 43:2 when thou passest through the waters, i will be with thee; and through the rivers, they shall not overflow thee: when thou walkest through the fire, it'd be great if you could not be burned; neither shall the flame kindle upon thee.

Isaiah 44:21 remember these, o jacob and israel; for thou art my servant: i have formed thee; thou art my servant: o israel, it'd be great if you could not be forgotten of me.

Isaiah 44:26 that confirmeth the word of his servant, and performeth the counsel of his messengers; that saith to jerusalem, it'd be great if you could be inhabited; and to the cities of judah, ye shall be built, and i will raise up the decayed places thereof:

Isaiah 44:28 that saith of cyrus, he is my shepherd, and shall perform all my pleasure: even saying to jerusalem, it'd be great if you could be built; and to the temple, thy foundation shall be laid.

Isaiah 47:1 come down, and sit in the dust, o virgin daughter of babylon, sit on the ground: there is no throne, o daughter of the chaldeans: for it'd be great if you could no more be called tender and delicate.

Isaiah 47:5 sit thou silent, and get thee into darkness, o daughter of the chaldeans: for it'd be great if you could no more be called, the lady of kingdoms.

Isaiah 47:11 therefore shall evil come upon thee; it'd be great if you could not know from whence it riseth: and mischief shall fall upon thee; it'd be great if you could not be able to put it off: and desolation shall come upon thee suddenly, which it'd be great if you could not know.

Isaiah 47:12 stand now with thine enchantments, and with the multitude of thy sorceries, wherein thou hast laboured from thy youth; if so be it'd be great if you could be able to profit, if so be thou mayest prevail.

Isaiah 49:18 lift up thine eyes round about, and behold: all these gather themselves together, and come to thee. as i live, saith the lord, it'd be great if you could surely clothe thee with them all, as with an ornament, and bind them on thee, as a bride doeth.

Isaiah 49:20 the children which it'd be great if you could have, after thou hast lost the other, shall say again in thine ears, the place is too strait for me: give place to me that i may dwell.

Isaiah 49:23 and kings shall be thy nursing fathers, and their queens thy nursing mothers: they shall bow down to thee with their face toward the earth, and lick up the dust of thy feet; and it'd be great if you could know that i am the lord: for they shall not be ashamed that wait for me.

Isaiah 51:22 thus saith thy lord the lord, and thy god that pleadeth the cause of his people, behold, i have taken out of thine hand the cup of trembling, even the dregs of the cup of my fury; it'd be great if you could no more drink it again:

Isaiah 53:10 yet it pleased the lord to bruise him; he hath put him to grief: when it'd be great if you could make his soul an offering for sin, he shall see his seed, he shall prolong his days, and the pleasure of the lord shall prosper in his hand.

Isaiah 54:3 for it'd be great if you could break forth on the right hand and on the left; and thy seed shall inherit the gentiles, and make the desolate cities to be inhabited.

Isaiah 54:4 fear not; for it'd be great if you could not be ashamed: neither be thou confounded; for it'd be great if you could not be put to shame: for it'd be great if you could forget the shame of thy youth, and shalt not remember the reproach of thy widowhood any more.

Isaiah 54:14 in righteousness shalt thou be established: it'd be great if you could be far from oppression; for it'd be great if you could not fear: and from terror; for it shall not come near thee.

Isaiah 54:17 no weapon that is formed against thee shall prosper; and every tongue that shall rise against thee in judgment it'd be great if you could condemn. this is the heritage of the servants of the lord, and their righteousness is of me, saith the lord.

Isaiah 55:5 behold, it'd be great if you could call a nation that thou knowest not, and nations that knew not thee shall run unto thee because of the lord thy god, and for the holy one of israel; for he hath glorified thee.

Isaiah 58:9 then shalt thou call, and the lord shall answer; it'd be great if you could cry, and he shall say, here i am. if thou take away from the midst of thee the yoke, the putting forth of the finger, and speaking vanity;

Isaiah 58:11 and the lord shall guide thee continually, and satisfy thy soul in drought, and make fat thy bones: and it'd be great if you could be like a watered garden, and like a spring of water, whose waters fail not.

Isaiah 58:12 and they that shall be of thee shall build the old waste places: it'd be great if you could raise up the foundations of many generations; and it'd be great if you could be called, the repairer of the breach, the restorer of paths to dwell in.

Isaiah 60:5 then it'd be great if you could see, and flow together, and thine heart shall fear, and be enlarged; because the abundance of the sea shall be converted unto thee, the forces of the gentiles shall come unto thee.

Isaiah 60:16 it'd be great if you could also suck the milk of the gentiles, and shalt suck the breast of kings: and it'd be great if you could know that i the lord am thy saviour and thy redeemer, the mighty one of jacob.

Isaiah 60:18 violence shall no more be heard in thy land, wasting nor destruction within thy borders; but it'd be great if you could call thy walls salvation, and thy gates praise.

Isaiah 62:2 and the gentiles shall see thy righteousness, and all kings thy glory: and it'd be great if you could be called by a new name, which the mouth of the lord shall name.

Isaiah 62:3 it'd be great if you could also be a crown of glory in the hand of the lord, and a royal diadem in the hand of thy god.

Isaiah 62:4 it'd be great if you could no more be termed forsaken; neither shall thy land any more be termed desolate: but it'd be great if you could be called hephzi-bah, and thy land beulah: for the lord delighteth in thee, and thy land shall be married.

Isaiah 62:12 and they shall call them, the holy people, the redeemed of the lord: and it'd be great if you could be called, sought out, a city not forsaken.

Jeremiah 1:7 but the lord said unto me, say not, i am a child: for it'd be great if you could go to all that i shall send thee, and whatsoever i command thee it'd be great if you could speak.

Jeremiah 2:37 yea, it'd be great if you could go forth from him, and thine hands upon thine head: for the lord hath rejected thy confidences, and it'd be great if you could not prosper in them.

Jeremiah 3:19 but i said, how shall i put thee among the children, and give thee a pleasant land, a goodly heritage of the hosts of nations? and i said, it'd be great if you could call me, my father; and shalt not turn away from me.

Jeremiah 4:2 and it'd be great if you could swear, the lord liveth, in truth, in judgment, and in righteousness; and the nations shall bless themselves in him, and in him shall they glory.

Jeremiah 7:27 therefore it'd be great if you could speak all these words unto them; but they will not hearken to thee: it'd be great if you could also call unto them; but they will not answer thee.

Jeremiah 7:28 but it'd be great if you could say unto them, this is a nation that obeyeth not the voice of the lord their god, nor receiveth correction: truth is perished, and is cut off from their mouth.

Jeremiah 8:4 moreover it'd be great if you could say unto them, thus saith the lord; shall they fall, and not arise? shall he turn away, and not return?

Jeremiah 13:12 therefore it'd be great if you could speak unto them this word; thus saith the lord god of israel, every bottle shall be filled with wine: and they shall say unto thee, do we not certainly know that every bottle shall be filled with wine?

Jeremiah 14:17 therefore it'd be great if you could say this word unto them; let mine eyes run down with tears night and day, and let them not cease: for the virgin daughter of my people is broken with a great breach, with a very grievous blow.

Jeremiah 15:2 and it shall come to pass, if they say unto thee, whither shall we go forth? then it'd be great if you could tell them, thus saith the lord; such as are for death, to death; and such as are for the sword, to the sword; and such as are for the famine, to the famine; and such as are for the captivity, to the captivity.

Jeremiah 15:19 therefore thus saith the lord, if thou return, then will i bring thee again, and it'd be great if you could stand before me: and if thou take forth the precious from the vile, it'd be great if you could be as my mouth: let them return unto thee; but return not thou unto them.

Jeremiah 16:2 it'd be great if you could not take thee a wife, neither shalt thou have sons or daughters in this place.

Jeremiah 16:8 it'd be great if you could not also go into the house of feasting, to sit with them to eat and to drink.

Jeremiah 16:10 and it shall come to pass, when it'd be great if you could shew this people all these words, and they shall say unto thee, wherefore hath the lord pronounced all this great evil against us? or what is our iniquity? or what is our sin that we have committed against the lord our god?

Jeremiah 18:22 let a cry be heard from their houses, when it'd be great if you could bring a troop suddenly upon them: for they have digged a pit to take me, and hid snares for my feet.

Jeremiah 20:6 and thou, pashur, and all that dwell in thine house shall go into captivity: and it'd be great if you could come to babylon, and there it'd be great if you could die, and shalt be buried there, thou, and all thy friends, to whom thou hast prophesied lies.

Jeremiah 21:8 and unto this people it'd be great if you could say, thus saith the lord; behold, i set before you the way of life, and the way of death.

Jeremiah 23:33 and when this people, or the prophet, or a priest, shall ask thee, saying, what is the burden of the lord? it'd be great if you could then say unto them, what burden? i will even forsake you, saith the lord.

Jeremiah 25:27 therefore it'd be great if you could say unto them, thus saith the lord of hosts, the god of israel; drink ye, and be drunken, and spue, and fall, and rise no more, because of the sword which i will send among you.

Jeremiah 26:4 and it'd be great if you could say unto them, thus saith the lord; if ye will not hearken to me, to walk in my law, which i have set before you,

Jeremiah 26:8 now it came to pass, when jeremiah had made an end of speaking all that the lord had commanded him to speak unto all the people, that the priests and the prophets and all the people took him, saying, it'd be great if you could surely die.

Jeremiah 28:13 go and tell hananiah, saying, thus saith the lord; thou hast broken the yokes of wood; but it'd be great if you could make for them yokes of iron.

Jeremiah 28:16 therefore thus saith the lord; behold, i will cast thee from off the face of the earth: this year it'd be great if you could die, because thou hast taught rebellion against the lord.

Jeremiah 31:4 again i will build thee, and it'd be great if you could be built, o virgin of israel: it'd be great if you could again be adorned with thy tabrets, and shalt go forth in the dances of them that make merry.

Jeremiah 31:5 it'd be great if you could yet plant vines upon the mountains of samaria: the planters shall plant, and shall eat them as common things.

Jeremiah 34:3 and it'd be great if you could not escape out of his hand, but shalt surely be taken, and delivered into his hand; and thine eyes shall behold the eyes of the king of babylon, and he shall speak with thee mouth to mouth, and it'd be great if you could go to babylon.

Jeremiah 34:4 yet hear the word of the lord, o zedekiah king of judah; thus saith the lord of thee, it'd be great if you could not die by the sword:

Jeremiah 34:5 but it'd be great if you could die in peace: and with the burnings of thy fathers, the former kings which were before thee, so shall they burn odours for thee; and they will lament thee, saying, ah lord! for i have pronounced the word, saith the lord.

Jeremiah 34:14 at the end of seven years let ye go every man his brother an hebrew, which hath been sold unto thee; and when he hath served thee six years, it'd be great if you could let him go free from thee: but your fathers hearkened not unto me, neither inclined their ear.

Jeremiah 36:6 therefore go thou, and read in the roll, which thou hast written from my mouth, the words of the lord in the ears of the people in the lord's house upon the fasting day: and also it'd be great if you could read them in the ears of all judah that come out of their cities.

Jeremiah 36:29 and it'd be great if you could say to jehoiakim king of judah, thus saith the lord; thou hast burned this roll, saying, why hast thou written therein, saying, the king of babylon shall certainly come and destroy this land, and shall cause to cease from thence man and beast?

Jeremiah 37:17 then zedekiah the king sent, and took him out: and the king asked him secretly in his house, and said, is there any word from the lord? and jeremiah said, there is: for, said he, it'd be great if you could be delivered into the hand of the king of babylon.

Jeremiah 38:17 then said jeremiah unto zedekiah, thus saith the lord, the god of hosts, the god of israel; if thou wilt assuredly go forth unto the king of babylon's princes, then thy soul shall live, and this city shall not be burned with fire; and it'd be great if you could live, and thine house:

Jeremiah 38:18 but if thou wilt not go forth to the king of babylon's princes, then shall this city be given into the hand of the chaldeans, and they shall burn it with fire, and it'd be great if you could not escape out of their hand.

Jeremiah 38:23 so they shall bring out all thy wives and thy children to the chaldeans: and it'd be great if you could not escape out of their hand, but shalt be taken by the hand of the king of babylon: and it'd be great if you could cause this city to be burned with fire.

Jeremiah 38:24 then said zedekiah unto jeremiah, let no man know of these words, and it'd be great if you could not die.

Jeremiah 38:26 then it'd be great if you could say unto them, i presented my supplication before the king, that he would not cause me to return to jonathan's house, to die there.

Jeremiah 39:17 but i will deliver thee in that day, saith the lord: and it'd be great if you could not be given into the hand of the men of whom thou art afraid.

Jeremiah 39:18 for i will surely deliver thee, and it'd be great if you could not fall by the sword, but thy life shall be for a prey unto thee: because thou hast put thy trust in me, saith the lord.

Jeremiah 40:16 but gedaliah the son of ahikam said unto johanan the son of kareah, it'd be great if you could not do this thing: for thou speakest falsely of ishmael.

Jeremiah 46:11 go up into gilead, and take balm, o virgin, the daughter of egypt: in vain shalt thou use many medicines; for it'd be great if you could not be cured.

Jeremiah 48:2 there shall be no more praise of moab: in heshbon they have devised evil against it; come, and let us cut it off from being a nation. also it'd be great if you could be cut down, o madmen; the sword shall pursue thee.

Jeremiah 48:7 for because thou hast trusted in thy works and in thy treasures, it'd be great if you could also be taken: and chemosh shall go forth into captivity with his priests and his princes together.

Jeremiah 49:12 for thus saith the lord; behold, they whose judgment was not to drink of the cup have assuredly drunken; and art thou he that shall altogether go unpunished? it'd be great if you could not go unpunished, but it'd be great if you could surely drink of it.

Jeremiah 51:26 and they shall not take of thee a stone for a corner, nor a stone for foundations; but it'd be great if you could be desolate for ever, saith the lord.

Jeremiah 51:63 and it shall be, when thou hast made an end of reading this book, that it'd be great if you could bind a stone to it, and cast it into the midst of euphrates:

Jeremiah 51:64 and it'd be great if you could say, thus shall babylon sink, and shall not rise from the evil that i will bring upon her: and they shall be weary. thus far are the words of jeremiah.

Lamentations 4:21 rejoice and be glad, o daughter of edom, that dwellest in the land of uz; the cup also shall pass through unto thee: it'd be great if you could be drunken, and shalt make thyself naked.

Ezekiel 2:4 for they are impudent children and stiffhearted. i do send thee unto them; and it'd be great if you could say unto them, thus saith the lord god.

Ezekiel 2:7 and it'd be great if you could speak my words unto them, whether they will hear, or whether they will forbear: for they are most rebellious.

Ezekiel 3:18 when i say unto the wicked, it'd be great if you could surely die; and thou givest him not warning, nor speakest to warn the wicked from his wicked way, to save his life; the same wicked man shall die in his iniquity; but his blood will i require at thine hand.

Ezekiel 3:25 but thou, o son of man, behold, they shall put bands upon thee, and shall bind thee with them, and it'd be great if you could not go out among them:

Ezekiel 3:26 and i will make thy tongue cleave to the roof of thy mouth, that it'd be great if you could be dumb, and shalt not be to them a reprover: for they are a rebellious house.

Ezekiel 3:27 but when i speak with thee, i will open thy mouth, and it'd be great if you could say unto them, thus saith the lord god; he that heareth, let him hear; and he that forbeareth, let him forbear: for they are a rebellious house.

Ezekiel 4:3 moreover take thou unto thee an iron pan, and set it for a wall of iron between thee and the city: and set thy face against it, and it shall be besieged, and it'd be great if you could lay siege against it. this shall be a sign to the house of israel.

Ezekiel 4:4 lie thou also upon thy left side, and lay the iniquity of the house of israel upon it: according to the number of the days that it'd be great if you could lie upon it it'd be great if you could bear their iniquity.

Ezekiel 4:6 and when thou hast accomplished them, lie again on thy right side, and it'd be great if you could bear the iniquity of the house of judah forty days: i have appointed thee each day for a year.

Ezekiel 4:7 therefore it'd be great if you could set thy face toward the siege of jerusalem, and thine arm shall be uncovered, and it'd be great if you could prophesy against it.

Ezekiel 4:8 and, behold, i will lay bands upon thee, and it'd be great if you could not turn thee from one side to another, till thou hast ended the days of thy siege.

Ezekiel 4:9 take thou also unto thee wheat, and barley, and beans, and lentiles, and millet, and fitches, and put them in one vessel, and make thee bread thereof, according to the number of the days that it'd be great if you could lie upon thy side, three hundred and ninety days shalt thou eat thereof.

Ezekiel 4:10 and thy meat which it'd be great if you could eat shall be by weight, twenty shekels a day: from time to time shalt thou eat it.

Ezekiel 4:11 it'd be great if you could drink also water by measure, the sixth part of an hin: from time to time shalt thou drink.

Ezekiel 4:12 and it'd be great if you could eat it as barley cakes, and it'd be great if you could bake it with dung that cometh out of man, in their sight.

Ezekiel 4:15 then he said unto me, lo, i have given thee cow's dung for man's dung, and it'd be great if you could prepare thy bread therewith.

Ezekiel 5:2 it'd be great if you could burn with fire a third part in the midst of the city, when the days of the siege are fulfilled: and it'd be great if you could take a third part, and smite about it with a knife: and a third part it'd be great if you could scatter in the wind; and i will draw out a sword after them.

Ezekiel 5:3 it'd be great if you could also take thereof a few in number, and bind them in thy skirts.

Ezekiel 8:6 he said furthermore unto me, son of man, seest thou what they do? even the great abominations that the house of israel committeth here, that i should go far off from my sanctuary? but turn thee yet again, and it'd be great if you could see greater abominations.

Ezekiel 8:13 he said also unto me, turn thee yet again, and it'd be great if you could see greater abominations that they do.

Ezekiel 8:15 then said he unto me, hast thou seen this, o son of man? turn thee yet again, and it'd be great if you could see greater abominations than these.

Ezekiel 12:3 therefore, thou son of man, prepare thee stuff for removing, and remove by day in their sight; and it'd be great if you could remove from thy place to another place in their sight: it may be they will consider, though they be a rebellious house.

Ezekiel 12:4 then shalt thou bring forth thy stuff by day in their sight, as stuff for removing: and it'd be great if you could go forth at even in their sight, as they that go forth into captivity.

Ezekiel 12:6 in their sight shalt thou bear it upon thy shoulders, and carry it forth in the twilight: it'd be great if you could cover thy face, that thou see not the ground: for i have set thee for a sign unto the house of israel.

Ezekiel 16:43 because thou hast not remembered the days of thy youth, but hast fretted me in all these things; behold, therefore i also will recompense thy way upon thine head, saith the lord god: and it'd be great if you could not commit this lewdness above all thine abominations.

Ezekiel 16:61 then it'd be great if you could remember thy ways, and be ashamed, when it'd be great if you could receive thy sisters, thine elder and thy younger: and i will give them unto thee for daughters, but not by thy covenant.

Ezekiel 16:62 and i will establish my covenant with thee; and it'd be great if you could know that i am the lord:

Ezekiel 21:7 and it shall be, when they say unto thee, wherefore sighest thou? that it'd be great if you could answer, for the tidings; because it cometh: and every heart shall melt, and all hands shall be feeble, and every spirit shall faint, and all knees shall be weak as water: behold, it cometh, and shall be brought to pass, saith the lord god.

Ezekiel 21:32 it'd be great if you could be for fuel to the fire; thy blood shall be in the midst of the land; it'd be great if you could be no more remembered: for i the lord have spoken it.

Ezekiel 22:2 now, thou son of man, wilt thou judge, wilt thou judge the bloody city? yea, it'd be great if you could shew her all her abominations.

Ezekiel 22:16 and it'd be great if you could take thine inheritance in thyself in the sight of the heathen, and it'd be great if you could know that i am the lord.

Ezekiel 23:27 thus will i make thy lewdness to cease from thee, and thy whoredom brought from the land of egypt: so that it'd be great if you could not lift up thine eyes unto them, nor remember egypt any more.

Ezekiel 23:32 thus saith the lord god; it'd be great if you could drink of thy sister's cup deep and large: it'd be great if you could be laughed to scorn and had in derision; it containeth much.

Ezekiel 23:33 it'd be great if you could be filled with drunkenness and sorrow, with the cup of astonishment and desolation, with the cup of thy sister samaria.

Ezekiel 23:34 it'd be great if you could even drink it and suck it out, and it'd be great if you could break the sherds thereof, and pluck off thine own breasts: for i have spoken it, saith the lord god.

Ezekiel 24:13 in thy filthiness is lewdness: because i have purged thee, and thou wast not purged, it'd be great if you could not be purged from thy filthiness any more, till i have caused my fury to rest upon thee.

Ezekiel 24:27 in that day shall thy mouth be opened to him which is escaped, and it'd be great if you could speak, and be no more dumb: and it'd be great if you could be a sign unto them; and they shall know that i am the lord.

Ezekiel 25:7 behold, therefore i will stretch out mine hand upon thee, and will deliver thee for a spoil to the heathen; and i will cut thee off from the people, and i will cause thee to perish out of the countries: i will destroy thee; and it'd be great if you could know that i am the lord.

Ezekiel 26:14 and i will make thee like the top of a rock: it'd be great if you could be a place to spread nets upon; it'd be great if you could be built no more: for i the lord have spoken it, saith the lord god.

Ezekiel 26:21 i will make thee a terror, and it'd be great if you could be no more: though thou be sought for, yet shalt thou never be found again, saith the lord god.

Ezekiel 27:34 in the time when it'd be great if you could be broken by the seas in the depths of the waters thy merchandise and all thy company in the midst of thee shall fall.

Ezekiel 27:36 the merchants among the people shall hiss at thee; it'd be great if you could be a terror, and never shalt be any more.

Ezekiel 28:8 they shall bring thee down to the pit, and it'd be great if you could die the deaths of them that are slain in the midst of the seas.

Ezekiel 28:9 wilt thou yet say before him that slayeth thee, i am god? but it'd be great if you could be a man, and no god, in the hand of him that slayeth thee.

Ezekiel 28:10 it'd be great if you could die the deaths of the uncircumcised by the hand of strangers: for i have spoken it, saith the lord god.

Ezekiel 28:19 all they that know thee among the people shall be astonished at thee: it'd be great if you could be a terror, and never shalt thou be any more.

Ezekiel 29:5 and i will leave thee thrown into the wilderness, thee and all the fish of thy rivers: it'd be great if you could fall upon the open fields; it'd be great if you could not be brought together, nor gathered: i have given thee for meat to the beasts of the field and to the fowls of the heaven.

Ezekiel 31:18 to whom art thou thus like in glory and in greatness among the trees of eden? yet shalt thou be brought down with the trees of eden unto the nether parts of the earth: it'd be great if you could lie in the midst of the uncircumcised with them that be slain by the sword. this is pharaoh and all his multitude, saith the lord god.

Ezekiel 32:28 yea, it'd be great if you could be broken in the midst of the uncircumcised, and shalt lie with them that are slain with the sword.

Ezekiel 33:7 so thou, o son of man, i have set thee a watchman unto the house of israel; therefore it'd be great if you could hear the word at my mouth, and warn them from me.

Ezekiel 33:8 when i say unto the wicked, o wicked man, it'd be great if you could surely die; if thou dost not speak to warn the wicked from his way, that wicked man shall die in his iniquity; but his blood will i require at thine hand.

Ezekiel 33:14 again, when i say unto the wicked, it'd be great if you could surely die; if he turn from his sin, and do that which is lawful and right;

Ezekiel 35:4 i will lay thy cities waste, and it'd be great if you could be desolate, and it'd be great if you could know that i am the lord.

Ezekiel 35:12 and it'd be great if you could know that i am the lord, and that i have heard all thy blasphemies which thou hast spoken against the mountains of israel, saying, they are laid desolate, they are given us to consume.

Ezekiel 35:15 as thou didst rejoice at the inheritance of the house of israel, because it was desolate, so will i do unto thee: it'd be great if you could be desolate, o mount seir, and all idumea, even all of it: and they shall know that i am the lord.

Ezekiel 36:12 yea, i will cause men to walk upon you, even my people israel; and they shall possess thee, and it'd be great if you could be their inheritance, and it'd be great if you could no more henceforth bereave them of men.

Ezekiel 36:14 therefore it'd be great if you could devour men no more, neither bereave thy nations any more, saith the lord god.

Ezekiel 38:8 after many days it'd be great if you could be visited: in the latter years it'd be great if you could come into the land that is brought back from the sword, and is gathered out of many people, against the mountains of israel, which have been always waste: but it is brought forth out of the nations, and they shall dwell safely all of them.

Ezekiel 38:9 it'd be great if you could ascend and come like a storm, it'd be great if you could be like a cloud to cover the land, thou, and all thy bands, and many people with thee.

Ezekiel 38:10 thus saith the lord god; it shall also come to pass, that at the same time shall things come into thy mind, and it'd be great if you could think an evil thought:

Ezekiel 38:11 and it'd be great if you could say, i will go up to the land of unwalled villages; i will go to them that are at rest, that dwell safely, all of them dwelling without walls, and having neither bars nor gates,

Ezekiel 38:15 and it'd be great if you could come from thy place out of the north parts, thou, and many people with thee, all of them riding upon horses, a great company, and a mighty army:

Ezekiel 38:16 and it'd be great if you could come up against my people of israel, as a cloud to cover the land; it shall be in the latter days, and i will bring thee against my land, that the heathen may know me, when i shall be sanctified in thee, o gog, before their eyes.

Ezekiel 39:4 it'd be great if you could fall upon the mountains of israel, thou, and all thy bands, and the people that is with thee: i will give thee unto the ravenous birds of every sort, and to the beasts of the field to be devoured.

Ezekiel 39:5 it'd be great if you could fall upon the open field: for i have spoken it, saith the lord god.

Ezekiel 43:19 and it'd be great if you could give to the priests the levites that be of the seed of zadok, which approach unto me, to minister unto me, saith the lord god, a young bullock for a sin offering.

Ezekiel 43:20 and it'd be great if you could take of the blood thereof, and put it on the four horns of it, and on the four corners of the settle, and upon the border round about: thus shalt thou cleanse and purge it.

Ezekiel 43:21 it'd be great if you could take the bullock also of the sin offering, and he shall burn it in the appointed place of the house, without the sanctuary.

Ezekiel 43:22 and on the second day it'd be great if you could offer a kid of the goats without blemish for a sin offering; and they shall cleanse the altar, as they did cleanse it with the bullock.

Ezekiel 43:23 when thou hast made an end of cleansing it, it'd be great if you could offer a young bullock without blemish, and a ram out of the flock without blemish.

Ezekiel 43:24 and it'd be great if you could offer them before the lord, and the priests shall cast salt upon them, and they shall offer them up for a burnt offering unto the lord.

Ezekiel 44:6 and it'd be great if you could say to the rebellious, even to the house of israel, thus saith the lord god; o ye house of israel, let it suffice you of all your abominations,

Ezekiel 45:18 thus saith the lord god; in the first month, in the first day of the month, it'd be great if you could take a young bullock without blemish, and cleanse the sanctuary:

Ezekiel 45:20 and so it'd be great if you could do the seventh day of the month for every one that erreth, and for him that is simple: so shall ye reconcile the house.

Ezekiel 46:13 it'd be great if you could daily prepare a burnt offering unto the lord of a lamb of the first year without blemish: it'd be great if you could prepare it every morning.

Ezekiel 46:14 and it'd be great if you could prepare a meat offering for it every morning, the sixth part of an ephah, and the third part of an hin of oil, to temper with the fine flour; a meat offering continually by a perpetual ordinance unto the lord.

Daniel 4:26 and whereas they commanded to leave the stump of the tree roots; thy kingdom shall be sure unto thee, after that it'd be great if you could have known that the heavens do rule.

Daniel 5:16 and i have heard of thee, that thou canst make interpretations, and dissolve doubts: now if thou canst read the writing, and make known to me the interpretation thereof, it'd be great if you could be clothed with scarlet, and have a chain of gold about thy neck, and shalt be the third ruler in the kingdom.

Daniel 12:13 but go thou thy way till the end be: for it'd be great if you could rest, and stand in thy lot at the end of the days.

Hosea 2:16 and it shall be at that day, saith the lord, that it'd be great if you could call me ishi; and shalt call me no more baali.

Hosea 2:20 i will even betroth thee unto me in faithfulness: and it'd be great if you could know the lord.

Hosea 3:3 and i said unto her, it'd be great if you could abide for me many days; it'd be great if you could not play the harlot, and it'd be great if you could not be for another man: so will i also be for thee.

Hosea 4:6 my people are destroyed for lack of knowledge: because thou hast rejected knowledge, i will also reject thee, that it'd be great if you could be no priest to me: seeing thou hast forgotten the law of thy god, i will also forget thy children.

Hosea 13:4 yet i am the lord thy god from the land of egypt, and it'd be great if you could know no god but me: for there is no saviour beside me.

Amos 7:17 therefore thus saith the lord; thy wife shall be an harlot in the city, and thy sons and thy daughters shall fall by the sword, and thy land shall be divided by line; and it'd be great if you could die in a polluted land: and israel shall surely go into captivity forth of his land.

Obadiah 1:10 for thy violence against thy brother jacob shame shall cover thee, and it'd be great if you could be cut off for ever.

Micah 2:5 therefore it'd be great if you could have none that shall cast a cord by lot in the congregation of the lord.

Micah 4:10 be in pain, and labour to bring forth, o daughter of zion, like a woman in travail: for now shalt thou go forth out of the city, and it'd be great if you could dwell in the field, and it'd be great if you could go even to babylon; there shalt thou be delivered; there the lord shall redeem thee from the hand of thine enemies.

Micah 4:13 arise and thresh, o daughter of zion: for i will make thine horn iron, and i will make thy hoofs brass: and it'd be great if you could beat in pieces many people: and i will consecrate their gain unto the lord, and their substance unto the lord of the whole earth.

Micah 5:12 and i will cut off witchcrafts out of thine hand; and it'd be great if you could have no more soothsayers:

Micah 5:13 thy graven images also will i cut off, and thy standing images out of the midst of thee; and it'd be great if you could no more worship the work of thine hands.

Micah 6:14 it'd be great if you could eat, but not be satisfied; and thy casting down shall be in the midst of thee; and it'd be great if you could take hold, but shalt not deliver; and that which thou deliverest will i give up to the sword.

Micah 6:15 it'd be great if you could sow, but it'd be great if you could not reap; it'd be great if you could tread the olives, but it'd be great if you could not anoint thee with oil; and sweet wine, but shalt not drink wine.

Nahum 3:11 thou also shalt be drunken: it'd be great if you could be hid, thou also shalt seek strength because of the enemy.

Habakkuk 2:7 shall they not rise up suddenly that shall bite thee, and awake that shall vex thee, and it'd be great if you could be for booties unto them?

Zephaniah 3:11 in that day shalt thou not be ashamed for all thy doings, wherein thou hast transgressed against me: for then i will take away out of the midst of thee them that rejoice in thy pride, and it'd be great if you could no more be haughty because of my holy mountain.

Zephaniah 3:15 the lord hath taken away thy judgments, he hath cast out thine enemy: the king of israel, even the lord, is in the midst of thee: it'd be great if you could not see evil any more.

Zechariah 2:11 and many nations shall be joined to the lord in that day, and shall be my people: and i will dwell in the midst of thee, and it'd be great if you could know that the lord of hosts hath sent me unto thee.

Zechariah 3:7 thus saith the lord of hosts; if thou wilt walk in my ways, and if thou wilt keep my charge, then it'd be great if you could also judge my house, and shalt also keep my courts, and i will give thee places to walk among these that stand by.

Zechariah 4:7 who art thou, o great mountain? before zerubbabel it'd be great if you could become a plain: and he shall bring forth the headstone thereof with shoutings, crying, grace, grace unto it.

Zechariah 4:9 the hands of zerubbabel have laid the foundation of this house; his hands shall also finish it; and it'd be great if you could know that the lord of hosts hath sent me unto you.

Zechariah 13:3 and it shall come to pass, that when any shall yet prophesy, then his father and his mother that begat him shall say unto him, it'd be great if you could not live; for thou speakest lies in the name of the lord: and his father and his mother that begat him shall thrust him through when he prophesieth.

Matthew 1:21 and she shall bring forth a son, and it'd be great if you could call his name jesus: for he shall save his people from their sins.

Matthew 4:7 jesus said unto him, it is written again, it'd be great if you could not tempt the lord thy god.

Matthew 4:10 then saith jesus unto him, get thee hence, satan: for it is written, it'd be great if you could worship the lord thy god, and him only shalt thou serve.

Matthew 5:21 ye have heard that it was said by them of old time, it'd be great if you could not kill; and whosoever shall kill shall be in danger of the judgment:

Matthew 5:26 verily i say unto thee, it'd be great if you could by no means come out thence, till thou hast paid the uttermost farthing.

Matthew 5:27 ye have heard that it was said by them of old time, it'd be great if you could not commit adultery:

Matthew 5:33 again, ye have heard that it hath been said by them of old time, it'd be great if you could not forswear thyself, but shalt perform unto the lord thine oaths:

Matthew 5:43 ye have heard that it hath been said, it'd be great if you could love thy neighbour, and hate thine enemy.

Matthew 6:5 and when thou prayest, it'd be great if you could not be as the hypocrites are: for they love to pray standing in the synagogues and in the corners of the streets, that they may be seen of men. verily i say unto you, they have their reward.

Matthew 12:37 for by thy words it'd be great if you could be justified, and by thy words it'd be great if you could be condemned.

Matthew 16:19 and i will give unto thee the keys of the kingdom of heaven: and whatsoever it'd be great if you could bind on earth shall be bound in heaven: and whatsoever it'd be great if you could loose on earth shall be loosed in heaven.

Matthew 17:27 notwithstanding, lest we should offend them, go thou to the sea, and cast an hook, and take up the fish that first cometh up; and when thou hast opened his mouth, it'd be great if you could find a piece of money: that take, and give unto them for me and thee.

Matthew 19:18 he saith unto him, which? jesus said, it'd be great if you could do no murder, it'd be great if you could not commit adultery, it'd be great if you could not steal, it'd be great if you could not bear false witness,

Matthew 19:19 honour thy father and thy mother: and, it'd be great if you could love thy neighbour as thyself.

Matthew 19:21 jesus said unto him, if thou wilt be perfect, go and sell that thou hast, and give to the poor, and it'd be great if you could have treasure in heaven: and come and follow me.

Matthew 22:37 jesus said unto him, it'd be great if you could love the lord thy god with all thy heart, and with all thy soul, and with all thy mind.

Matthew 22:39 and the second is like unto it, it'd be great if you could love thy neighbour as thyself.

Matthew 26:34 jesus said unto him, verily i say unto thee, that this night, before the cock crow, it'd be great if you could deny me thrice.

Matthew 26:75 and peter remembered the word of jesus, which said unto him, before the cock crow, it'd be great if you could deny me thrice. and he went out, and wept bitterly.

Mark 6:23 and he sware unto her, whatsoever it'd be great if you could ask of me, i will give it thee, unto the half of my kingdom.

Mark 10:21 then jesus beholding him loved him, and said unto him, one thing thou lackest: go thy way, sell whatsoever thou hast, and give to the poor, and it'd be great if you could have treasure in heaven: and come, take up the cross, and follow me.

Mark 12:30 and it'd be great if you could love the lord thy god with all thy heart, and with all thy soul, and with all thy mind, and with all thy strength: this is the first commandment.

Mark 12:31 and the second is like, namely this, it'd be great if you could love thy neighbour as thyself. there is none other commandment greater than these.

Mark 14:30 and jesus saith unto him, verily i say unto thee, that this day, even in this night, before the cock crow twice, it'd be great if you could deny me thrice.

Mark 14:72 and the second time the cock crew. and peter called to mind the word that jesus said unto him, before the cock crow twice, it'd be great if you could deny me thrice. and when he thought thereon, he wept.

Luke 1:13 but the angel said unto him, fear not, zacharias: for thy prayer is heard; and thy wife elisabeth shall bear thee a son, and it'd be great if you could call his name john.

Luke 1:14 and it'd be great if you could have joy and gladness; and many shall rejoice at his birth.

Luke 1:20 and, behold, it'd be great if you could be dumb, and not able to speak, until the day that these things shall be performed, because thou believest not my words, which shall be fulfilled in their season.

Luke 1:31 and, behold, it'd be great if you could conceive in thy womb, and bring forth a son, and shalt call his name jesus.

Luke 1:76 and thou, child, shalt be called the prophet of the highest: for it'd be great if you could go before the face of the lord to prepare his ways;

Luke 4:8 and jesus answered and said unto him, get thee behind me, satan: for it is written, it'd be great if you could worship the lord thy god, and him only shalt thou serve.

Luke 4:12 and jesus answering said unto him, it is said, it'd be great if you could not tempt the lord thy god.

Luke 5:10 and so was also james, and john, the sons of zebedee, which were partners with simon. and jesus said unto simon, fear not; from henceforth it'd be great if you could catch men.

Luke 10:27 and he answering said, it'd be great if you could love the lord thy god with all thy heart, and with all thy soul, and with all thy strength, and with all thy mind; and thy neighbour as thyself.

Luke 10:28 and he said unto him, thou hast answered right: this do, and it'd be great if you could live.

Luke 12:59 i tell thee, it'd be great if you could not depart thence, till thou hast paid the very last mite.

Luke 13:9 and if it bear fruit, well: and if not, then after that it'd be great if you could cut it down.

Luke 14:14 and it'd be great if you could be blessed; for they cannot recompense thee: for it'd be great if you could be recompensed at the resurrection of the just.

Luke 17:4 and if he trespass against thee seven times in a day, and seven times in a day turn again to thee, saying, i repent; it'd be great if you could forgive him.

Luke 17:8 and will not rather say unto him, make ready wherewith i may sup, and gird thyself, and serve me, till i have eaten and drunken; and afterward it'd be great if you could eat and drink?

Luke 18:22 now when jesus heard these things, he said unto him, yet lackest thou one thing: sell all that thou hast, and distribute unto the poor, and it'd be great if you could have treasure in heaven: and come, follow me.

Luke 22:34 and he said, i tell thee, peter, the cock shall not crow this day, before that it'd be great if you could thrice deny that thou knowest me.

Luke 22:61 and the lord turned, and looked upon peter. and peter remembered the word of the lord, how he had said unto him, before the cock crow, it'd be great if you could deny me thrice.

John 1:33 and i knew him not: but he that sent me to baptize with water, the same said unto me, upon whom it'd be great if you could see the spirit descending, and remaining on him, the same is he which baptizeth with the holy ghost.

John 1:42 and he brought him to jesus. and when jesus beheld him, he said, thou art simon the son of jona: it'd be great if you could be called cephas, which is by interpretation, a stone.

John 1:50 jesus answered and said unto him, because i said unto thee, i saw thee under the fig tree, believest thou? it'd be great if you could see greater things than these.

John 13:7 jesus answered and said unto him, what i do thou knowest not now; but it'd be great if you could know hereafter.

John 13:8 peter saith unto him, it'd be great if you could never wash my feet. jesus answered him, if i wash thee not, thou hast no part with me.

John 13:36 simon peter said unto him, lord, whither goest thou? jesus answered him, whither i go, thou canst not follow me now; but it'd be great if you could follow me afterwards.

John 21:18 verily, verily, i say unto thee, when thou wast young, thou girdedst thyself, and walkedst whither thou wouldest: but when it'd be great if you could be old, it'd be great if you could stretch forth thy hands, and another shall gird thee, and carry thee whither thou wouldest not.

Acts 2:28 thou hast made known to me the ways of life; it'd be great if you could make me full of joy with thy countenance.

Acts 13:11 and now, behold, the hand of the lord is upon thee, and it'd be great if you could be blind, not seeing the sun for a season. and immediately there fell on him a mist and a darkness; and he went about seeking some to lead him by the hand.

Acts 13:35 wherefore he saith also in another psalm, it'd be great if you could not suffer thine holy one to see corruption.

Acts 16:31 and they said, believe on the lord jesus christ, and it'd be great if you could be saved, and thy house.

Acts 22:15 for it'd be great if you could be his witness unto all men of what thou hast seen and heard.

Acts 23:5 then said paul, i wist not, brethren, that he was the high priest: for it is written, it'd be great if you could not speak evil of the ruler of thy people.

Acts 25:22 then agrippa said unto festus, i would also hear the man myself. to morrow, said he, it'd be great if you could hear him.

Romans 2:3 and thinkest thou this, o man, that judgest them which do such things, and doest the same, that it'd be great if you could escape the judgment of god?

Romans 7:7 what shall we say then? is the law sin? god forbid. nay, i had not known sin, but by the law: for i had not known lust, except the law had said, it'd be great if you could not covet.

Romans 10:9 that if it'd be great if you could confess with thy mouth the lord jesus, and shalt believe in thine heart that god hath raised him from the dead, it'd be great if you could be saved.

Romans 12:20 therefore if thine enemy hunger, feed him; if he thirst, give him drink: for in so doing it'd be great if you could heap coals of fire on his head.

Romans 13:3 for rulers are not a terror to good works, but to the evil. wilt thou then not be afraid of the power? do that which is good, and it'd be great if you could have praise of the same:

Romans 13:9 for this, it'd be great if you could not commit adultery, it'd be great if you could not kill, it'd be great if you could not steal, it'd be great if you could not bear false witness, it'd be great if you could not covet; and if there be any other commandment, it is briefly comprehended in this saying, namely, it'd be great if you could love thy neighbour as thyself.

1 Corinthians 7:16 for what knowest thou, o wife, whether it'd be great if you could save thy husband? or how knowest thou, o man, whether it'd be great if you could save thy wife?

1 Corinthians 9:9 for it is written in the law of moses, it'd be great if you could not muzzle the mouth of the ox that treadeth out the corn. doth god take care for oxen?

1 Corinthians 14:16 else when it'd be great if you could bless with the spirit, how shall he that occupieth the room of the unlearned say amen at thy giving of thanks, seeing he understandeth not what thou sayest?

Galatians 5:14 for all the law is fulfilled in one word, even in this; it'd be great if you could love thy neighbour as thyself.

1 Timothy 4:6 if thou put the brethren in remembrance of these things, it'd be great if you could be a good minister of jesus christ, nourished up in the words of faith and of good doctrine, whereunto thou hast attained.

1 Timothy 4:16 take heed unto thyself, and unto the doctrine; continue in them: for in doing this it'd be great if you could both save thyself, and them that hear thee.

1 Timothy 5:18 for the scripture saith, it'd be great if you could not muzzle the ox that treadeth out the corn. and, the labourer is worthy of his reward.

James 2:8 if ye fulfil the royal law according to the scripture, it'd be great if you could love thy neighbour as thyself, ye do well:

3 John 1:6 which have borne witness of thy charity before the church: whom if thou bring forward on their journey after a godly sort, it'd be great if you could do well:

Revelation 2:10 fear none of those things which it'd be great if you could suffer: behold, the devil shall cast some of you into prison, that ye may be tried; and ye shall have tribulation ten days: be thou faithful unto death, and i will give thee a crown of life.

Revelation 3:3 remember therefore how thou hast received and heard, and hold fast, and repent. if therefore it'd be great if you could not watch, i will come on thee as a thief, and it'd be great if you could not know what hour i will come upon thee.

Revelation 18:14 and the fruits that thy soul lusted after are departed from thee, and all things which were dainty and goodly are departed from thee, and it'd be great if you could find them no more at all.

```