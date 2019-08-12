# Episode 6

WEBVTT

00:00:11.840 --> 00:00:35.230
<v John Sundell>Welcome to the swift community podcast. I am John Sindel. And on this episode, we're going to discuss Swift you I and share some of our first impressions of this exciting new framework and how we think it's going to impact the Swift _and Iowa's developer communities._ And to do that, I have three wonderful people joining me on this episode. First up is Kateryna Gridina . Welcome to the show, Kateryna.

00:00:35.470 --> 00:00:46.350
<v Kateryna Gridina>Hi, John. Um, hello, everyone. My name is Katerina ~~Workings. Alana~~ I'm working in Zalando and I just started to play ~~with you, if you're I,~~  with SwiftUI, like, four weeks ago, but already very excited about this.

00:00:46.360 --> 00:00:50.040
<v John Sundell>Awesome. And next up, we have Paul Hudson. Welcome, Paul.

00:00:50.100 --> 00:00:55.400
<v Paul Hudson>Hey, folks. _My polar run hacking with Swift_ and I am currently obsessed with ~~you.~~ SwiftUI. It's great fun.

00:00:55.690 --> 00:01:00.410
<v John Sundell>Awesome. And last but not least, we have Erica Sadun. Welcome, Erica.

00:01:00.420 --> 00:01:11.730
<v Erica Sadun>Hi. Uh, this is Erica Sadun, and I'm talking from ~~Tessa Ll Island~~ Tessel Island , where I am currently participating in Swift Island of Conference over here with these other two wonderful people.

00:01:11.880 --> 00:01:15.200
<v Paul Hudson>I keep telling folks here that actually she messed up the title. The Erica Sadun.

00:01:16.160 --> 00:01:43.170
<v John Sundell>That's amazing. So I am John Sundell. I am the creator of Swift by Sundell and just a swift developer in general. I love coding and swift writing about swift podcasting about Swift and everything in between. So about one month has now passed since SwiftUI was first introduced at WWDC 2019. So to get us started, I'd love to hear some of your first impressions when you first saw or heard about the announcement of SwiftUI 

00:01:43.360 --> 00:01:53.620
<v Erica Sadun>I think that it explained a lot about the mad rush of proposals that went through swift evolution in the past few months.

00:01:53.720 --> 00:02:06.660
<v John Sundell>Yeah, there's been a lot of changes to the language to support the declarative API, and with all the function builders and everything that's been added to Swift in order to accommodate the API of SwiftUI

00:02:06.795 --> 00:02:15.065
<v Paul Hudson>Well, it's more like we watching it developed for a while. _And you see these things coming in on give examples and rationales of how it could be used and well,_

00:02:15.255 --> 00:02:15.635
<v Paul Hudson>I can

00:02:15.635 --> 00:02:22.265
<v Paul Hudson>sort of see that. But I'm not really seeing the bigger picture here, and they were obviously working towards something where's weren't quite sure what or when.

00:02:22.595 --> 00:02:33.425
<v Erica Sadun>And of course, you know these are pretty exciting features everything from inferred returns to opaque return types and so forth. These are wonderful things

00:02:33.995 --> 00:02:45.845
<v Erica Sadun>and seeing them all to come together and be realized in SwiftUI. I has been one of the great pleasures of finally seeing the mystery unravel. 
  
00:02:45.855 --> 00:02:51.115
<v Kateryna Gridina>Yeah, and I think it's very excited also for old school people who really

00:02:51.625 --> 00:03:07.435
<v Kateryna Gridina>become like bored about the language. They wanted something you they wanted something exciting. And this was kind of a fresh air for everyone. And it was like something really new. You can learn basically new language within the same infrastructure

00:03:07.935 --> 00:03:28.955
<v Paul Hudson>_is willing you, right?_ Everyone saying that Wow, this is completely unlike everyone _seems home_. But I think folks who found it a little bit hard to see _something that the devil is that. Don't you see whether? _Okay, here's some code. It's all new SwiftUI Stuff on also what the dollar signs, what does @ signs. We've got new language changes, plus whole new. I think at the same time is _a lot mentally. Get over_. I think

00:03:29.395 --> 00:03:47.065
<v Erica Sadun>also, it's very early technology, and anybody who's actually tried to put, you know, get hands on with this has really faced either the burden of being very self reliant or might be dissuaded by the fact that there are so many cryptic fortune Cookie Titan.

00:03:49.995 --> 00:04:37.313
<v John Sundell>Yeah, the errors is definitely an issue that will need to be solved at one point or another. And, you know, when you start working with SwiftUI and you follow some of the tutorials or you do some of the kind of hello world style implementations. It's works great, and the code itself that you produce, even if it's quite sophisticated, looks really, really elegant and nice. But then, if you make a little mistake, for example, you used the wrong type somewhere or you forget like an argument, you can get these really obscure errors because it becomes quite obvious very quickly that swiftUI makes use of some of the very most advanced generics features of Swift and sometimes the type system and the diagnostics and the errors haven't really caught up with what SwiftUI wants to do,



00:04:37.493 --> 00:05:21.693
<v Erica Sadun>but it's not just catching up in that way. On Tuesday night, Paul and I were sitting, going over text fields, discovering that half of them had been deprecated with the Beta three release and the language is evolving so quickly. It's almost a microcosm of what we were seeing when Swift itself was first introduced. That it is only through getting people in a wide environment to really try it. That is finally getting field tested. And you're seeing that with a lot of the redesigns, the deprecation  the missing pieces. _This is very early tak_

00:05:22.123 --> 00:06:10.293
<v Paul Hudson>right, But you got in mind. That's you know, _the paper turn types from 251 survivor_ I knew it's not in SwiftUI yet. They are using that. They have some view for us. They're all their own internal code. You'll see angle, bracket, angle, bracket angle bracket. What if I contact? What if I did it? He doesn't use it yet. You get is really, really long stacks of pop fiction bracket everywhere. It could be awfully hard to read, _but does the language of open so quickly?_ I'm trying to think of another time where I've seen a language be so heavily adapted to fit a product on. If you think there has been a production now with so many years, potentially four longer years, they're making this a swift one. It was a completely different language. Back there once were two massive breaking things with three. These poor people have been writing their coats so many times get where it is today.

00:06:10.583 --> 00:06:14.783
<v Kateryna Gridina>Yeah, that's true for me was also a big struggle to deal with Errors.

00:06:15.663 --> 00:06:40.735
<v Kateryna Gridina>Because sometimes you have error in completely different place and because of this nasty views and messed it stacks and sometimes there error even with the data that you pass. But compiler don't tell you anything about it. So you need to kind of do your own way off. _Knew the bagging_, which was completely different, even with Swift. Because now it's kind of comment out, check something. Something that comment out another self check something else.

00:06:40.745 --> 00:06:43.315
<v Paul Hudson>_A way, not_

00:06:43.315 --> 00:06:50.115
<v Kateryna Gridina>It's not the normal debugging which is used to be before. _So it's also kind of shift off the bank. Use cases that you have._

00:06:50.125 --> 00:06:59.345
<v Paul Hudson>So you're teaching SwiftUI today, won't you? Yeah. _On dhe was a positive, good, responsible happy. Well, enjoy it while they're getting errors. Long, confusing things._

00:06:59.655 --> 00:07:36.885
<v Kateryna Gridina>It was kind of a lot of moments like Oh, I have an error in completely different place and now is there or I did everything right. _Just Exco doesn't respond properly or I do everything completely._ Okay? But it's not showing preview, but the chosen, the in the actual simulator. So they were, like, kind of those strange hours that we have. But people actually really, really like it. And I've seen that a lot of people were, like, so much into they even didn't listen to me sometimes because they like, Okay, I just shut up. I just need to finish my be self confidence. So

00:07:37.495 --> 00:08:17.955
<v John Sundell>yeah, it is really exciting. And I want to go back to something that you said there are a couple of minutes ago, Kateryna, where you said that it's kind of breathing a little bit of fresh air into UI developments for apples, platforms because I also felt the same way as you described that, you know, UI development was getting Maybe not boring is too strong of a word, but it was getting a bit repetitive. I felt like I was always making table views and collection views for over and over and over again. And with SwiftUI now it's like something brand new that you can dive into and learn. And for me it has really _re ignited_ my passion for building UI and animations and things like that, which I'm really excited about that aspect.

00:08:17.965 --> 00:08:33.095
<v Erica Sadun>But you do need to take into account that the entry path _that SwiftUI creating is very much towards_ the kinds of user experiences that we've seen before,

00:08:33.631 --> 00:08:36.541
<v Erica Sadun>including collection views in table views and,

00:08:37.091 --> 00:08:47.711
<v Erica Sadun>um, animations and so forth. _They're just making it much smoother of of half and smoother for people to come in. And you this_

00:08:48.301 --> 00:08:53.151
<v Erica Sadun>And it's interesting how much of what we're given

00:08:53.701 --> 00:09:00.861
<v Erica Sadun>is giving us the tools to make exactly the kinds of products that predominate on the Apple store.


00:09:01.151 --> 00:10:09.751
<v Paul Hudson>That's great. So in common problems, presumably things like, you know, you look as, as, said table views right. That's a lot of gaps on, but it makes me all these trivial. _There's almost no co two things anymore._ Same for the combined framework. Would have decoding of Jason built into one of the steps. Now, if it makes things so much easier for those kinds of common tasks, I think that's why unsurprisingly, _all the dub dub stage_ or they show tell these. Look how fast they are, _It's the dailies are amazing_, so it doesn't have the out of the box. And also I quite enjoy. Is that because, of course, _I West been around _a long time now the idea of, you know, big title navigation bars the idea of safe areas. The idea of dark mode didn't exist in ~~Iowa. S~~ iOS one has been strapped on, modified hacked around, layout guides introduced _or the workout worker as it_ happened on now of Course SwiftUI. Now the new foundation. That's the starting point of clean things. There's no weird workarounds required you get. Stay here is by default. You get system colors by default. You get large titles by default, which is fantastic. Of course, in four years time

00:10:10.471 --> 00:10:18.811
<v Paul Hudson>when iOS, you know, 17 or without with all new Yes, it's it's obviously triangular phones. Now we'll see what you have to look around,

00:10:19.301 --> 00:10:33.131
<v Erica Sadun>And I also want to point out that we are moving from one declaring of system for the most part, which was auto layout to a different declarative system, which is SwiftUI except SwiftUI is  cleaner, prettier, funner

00:10:33.871 --> 00:10:49.221
<v Erica Sadun>and fewer people are cursing at it, although anybody who's using the Betas really is cursing at it a lot. But I think the end outcome is going to be much happier developers, especially those who are focused on the business logic.

00:10:49.829 --> 00:11:12.719
<v Kateryna Gridina>I just want to point out that batter is always pain, and we remember when the speech came with. But we also had a lot of painful moments, and it always will be the case. So I guess we just need to kind of live with this and being more flexible about this. But about SwiftUI I like it removes a lot of boilerplate from creating like very trivial and very simple

00:11:13.369 --> 00:11:38.599
<v Kateryna Gridina>controls your eye elements, and it gives us a little bit more time and space to create something more excited. Maybe some new features to be more flexible in this case, and then maybe development of one application will take 34 days, and then we can be done with this and we can add extra next to some nice fancy animation or some I don't know, something related to notifications, or VR

00:11:43.689 --> 00:12:35.499
<v John Sundell>one thing I really like about SwiftUI also is that it kind of makes it easy to do the right thing, like the right path is becoming the easiest path. I mean again, setting aside the errors and the beta issues and these things was which I'm kind of assuming will be solved eventually. But the fact now that when you write your UI you get like things like dark mode support and the things you mentioned Paul like right to left languages, accessibility, all these things that are the right things to do and makes your app richer and easier to use for more people is also now the easiest thing to do. And that's great, because Erica, you can. You compared SwiftUI a little bit to auto layout and I would say with auto layout, it was very easy to not do the right thing. And it was easy to get like errors and exceptions that things like that at runtime and with SwiftUI. I feel like it. It nudges us all developers in kind of the right direction.

00:12:35.619 --> 00:12:42.579
<v Erica Sadun>Furthermore, in auto layout, we dealt with size classes which I think were completely 

00:12:43.109 --> 00:13:03.858
<v Erica Sadun>insufficient for describing the domain of user interface specifications. But now that removing into environments. I think that we're going in the right direction for bringing in things we already mentioned dark mood and so forth. But environments can describe a lot more than that.

00:13:04.228 --> 00:13:06.958
<v Paul Hudson>_Yeah, I think I made so many talked about_

00:13:07.488 --> 00:13:18.708
<v Paul Hudson>his mercy and getting it right . They always say, Please, please, please, come on. Just at the very least used dynamic type. Name goes, Yeah, Yeah, you do that then doesn't do it. And actually, it's kind of baked  In

00:13:19.238 --> 00:13:30.358
<v Paul Hudson>fact, you could choose not to have that you really want to, but by default, the font size there are a lot of the type sizes. So, I believe, eliminate a wide class of problems. Maps kind of overnight.

00:13:30.948 --> 00:13:44.568
<v Erica Sadun>And you get those automatically when you do auto complete because the names are right there. It is expected that when you set the font, that is the vocabulary, the language you're going to use to describe your text.

00:13:44.918 --> 00:13:46.458
<v Paul Hudson>_Yeah, well, it works both ways_. I

00:13:46.848 --> 00:14:17.408
<v Kateryna Gridina>also think that possibility is a big topic for a lot of different companies because people don't want to invest so much time, and sometimes they just forget about it, and maybe it was not so important topic for some companies, you know, like look, say the truth. Sometimes it's not just that important. And now when you can do this just out of the box without putting too much effort and it just basically it works. It's amazing. And I think a lot of people will be very grateful that you have this functionality.

00:14:18.108 --> 00:14:36.458
<v Paul Hudson>So Erica can ask you a question because, you know, you have, you know, _that brag a tall well,_ like a person. But you've been fairly central to the way swift evolution has come along. You had more approved a proposal than anybody else. _Really? Anyone apple or rejected?_ I realized that as well. I

00:14:36.468 --> 00:14:38.318
<v Erica Sadun>think I hold the record for rejected.

00:14:39.668 --> 00:14:41.728
<v Erica Sadun>I'm not sure I do. For approved,

00:14:41.728 --> 00:15:07.491
<v Paul Hudson>I've counted them. You're very far ahead. I wanna ask you is you know, we've seen you team particularly swift evolve from day one to where it today, and it was a rookie process to get in some parts on. I wonder what you're seeing. A similar year or two ahead for SwiftUI do this SwiftUI you're gonna _have a great week? Gamification x 50 y three expected._ Now folks will explode in SwiftUI 3

00:15:07.501 --> 00:15:11.751
<v Erica Sadun>I think a lot of people are saying, What took you so long?

00:15:12.731 --> 00:15:22.861
<v Erica Sadun>Reactive programming is so fundamental to the way that people do their work outside of the apple ecosystem.

00:15:23.531 --> 00:15:30.191
<v Erica Sadun>It's like apples there and saying, Look what we produced and everybody's saying, Well, yeah, you know, uh,

00:15:30.201 --> 00:15:31.191
<v Paul Hudson>is that a good job?

00:15:31.201 --> 00:15:43.881
<v Erica Sadun>Good job. Here's your sticker. Yeah, exactly that. So the fact is, we're getting in late, but we're getting him with a very clear vision of where it's going to be.

00:15:44.691 --> 00:15:50.891
<v Erica Sadun>And I think that we're going to see growth. The question is how much turbulence

00:15:51.461 --> 00:15:55.041
<v Erica Sadun>I'm going to see. Not so much the vision but the turbulence.

00:15:55.051 --> 00:15:56.481
<v Paul Hudson>SwiftUI Evolution.

00:15:57.181 --> 00:15:57.801
<v Paul Hudson>I call it

00:15:58.391 --> 00:16:00.701
<v Erica Sadun>well, swiftUI isn't Open source.

00:16:00.701 --> 00:16:01.801
<v Paul Hudson>No, it's not , no, no

00:16:02.051 --> 00:16:03.241
<v Erica Sadun> And



00:16:03.811 --> 00:16:47.431
<v Erica Sadun> swiftUI has driven a lot of _where Swift evolution. The or_ open source project is over the last six months, and there are some people who have gotten quite cranky about this because so much has come in terms of driving the language from inside the apple umbrella for a language that is technically open source but is the major tooling for major company and that has to be taken account when looking at SwiftUI we don't have access to it. It is under their umbrella. We do not have a direction for it. And that means that the changes can be quite profound without community input.

00:16:47.621 --> 00:16:49.571
<v Paul Hudson>Right? And also that the D S L stuff,

00:16:50.111 --> 00:17:08.080
<v Paul Hudson>which is a large part of the way SwiftUI looks and works, landed on WWDC Monday along with SwiftUI on that that that that _has a strange way to reveal a feature I always have had lately. We're running. It was real photo finishes here, I gather, but that must have set some folks backs up. Presumably_

00:17:08.410 --> 00:17:15.150
<v Erica Sadun>we'll tell. Tell me more about what this proposal was because I don't know if everybody listening will have heard about

00:17:15.160 --> 00:17:19.500
<v Paul Hudson>it. Is it is. This is Actually it's a barrage probe, isn't it? Because, you know, I think almost

00:17:19.500 --> 00:17:21.380
<v Paul Hudson>everything in 51 not

00:17:21.380 --> 00:17:31.120
<v Paul Hudson>everything but almost everything in 51 somehow linked back SwiftUI where, and it's hard to imagine what SwiftUI will look like without,

00:17:31.910 --> 00:17:44.620
<v Paul Hudson>you know, see this mission return return without some view without the DSL without function build without without without without without what would it look like? I literally can't even imagine it. My brain was so different, a different UI that I'd be much more cluttered for a start.

00:17:44.680 --> 00:17:46.850
<v Erica Sadun>It's incestuous. 

<v Paul Hudson>Is it?

00:17:47.640 --> 00:17:52.670
<v Erica Sadun>Well, I'm saying in that they seems the two technologies seem

00:17:53.210 --> 00:17:57.080
<v Erica Sadun>so intertwined with each other. Would you agree? 

Yeah.

00:17:57.280 --> 00:18:31.970
<v John Sundell>And what do you think that this would look like going forward? Because presumably this is not the initial and last version of SwiftUI API or the type of language features that it will require to evolve. So how do you feel like now this with your is out in the open that this will will work going forward with swift evolution. Do you feel like there will be more transparency or do you still feel like they will be very locked in between? And we will. We will see more of this kind of features that have already been implemented in SwiftUI and then after the fact being proposed on swift evolution.

00:18:32.240 --> 00:18:48.650
<v Kateryna Gridina>I think because of certain complexity of the SwiftUI that we have now on because it's just a new language. I  guess there was a certain risk on doing it open source. So people just come there and start to change too many things and it will

00:18:49.770 --> 00:19:10.920
<v Kateryna Gridina>be evolving too fast because it's already evolving too fast and it will be so complicated to catch up with it. So I guess it just kind of a trial for people to just check it out. And then maybe it will be open source. I hope it will be open source when it's a bit more stable. So changes and it will not be so crucial when they come from outside.

00:19:11.492 --> 00:19:17.622
<v Paul Hudson>I think you're right there. Assumes you involved community. You're gonna get community feedback. That's kind of we want really and

00:19:18.192 --> 00:19:52.112
<v Paul Hudson>retroactively. You can look at this some of the abolition proposals like SE 2 50 kind of a swift style guide, please. _Why do you want that straight? Guys do that on now._ We can see the generating swift code from UI And but as the question what kind of swift code we generate on that comes the style guide thing. Of course, that got very heavily discussed in air quotes. _I go fucking because he felt that that's always be controversially_, we can agree on _Taliban space has been my No._ _The other thing to do is SwiftUI in general,_ so it's difficult because they revolted, want to have their

00:19:52.112 --> 00:19:55.162
<v Erica Sadun>views. But you also have to think about the tooling

00:19:55.772 --> 00:20:07.212
<v Erica Sadun>in particular. I think that we really need to think about the fact that we're going with a functional, fluent approach and we have to deal with things like debugging.

00:20:07.972 --> 00:20:11.012
<v Erica Sadun>So how do you think Xcode going to respond?

00:20:11.302 --> 00:20:14.032
<v Paul Hudson>I think you'll have a really great response about four years time.

00:20:17.452 --> 00:20:21.512
<v Paul Hudson>Well, you don't mind. You know the Apple works silently.

00:20:22.092 --> 00:20:54.892
<v Paul Hudson>They work in very, very heavily divided silently where most folks don't know other folks working on on. So I expect something saying, You know, _I look in there on that kid._ I hadn't heard of SwiftUI, which _had an M K Matt View wrapper for SwiftUI on enforcement. Until that situation, no one does stop making those rappers_ _saying is true for a chunk of the X 30 mikes, but also quite involved. _They had to have the preview and stuff, but no, everyone knows and now everyone knows hopefully an outside line around visions and plans for next year or the year after. We'll see where it goes.

00:20:55.022 --> 00:21:33.203
<v John Sundell>So we talk now about some of the things that were excited about some of the initial problems with SwiftUI current states, like the pros and cons and things like that. And I think it's fair to say, like, this is very early technology. I think that's something we can all agree on whether or not you're excited about it or you're skeptical, it's It's early days and it still hasn't been fully formed yet. So one question that I know a lot of people in the community are asking themselves and each other is when is it a good time to start adopting this like, should you be an early adopter and dive right in? Should you maybe wait a little bit and see how this all plays out? What are your thoughts about when and how to adopt SwiftUI


// MARK: Stop here
00:21:33.343 --> 00:21:48.663
<v Kateryna Gridina>I I think it really depends on the product that you have. I guess if you have quite new product, which you don't have too many too many users in it, or maybe just experimental product where there is no high risks

00:21:49.743 --> 00:22:35.713
<v Kateryna Gridina>that something will go wrong, that I can think you can start experiment with it. But for example, in Jalandhar, when you have 40,000,000 users, it's very risky to introduce something like that. And it will break in a moment and you will not be able to fix it because of the review protests and so on and so forth. So we cannot treat the business in the same time. And one big disadvantage that I think is also stopping a lot of people to use it is that we have don't have backwards compatibility toe previous OS versions. And we have so many users that use R S 11 0 s 12. And I guess this will be the biggest issue in the future. So I expect like maybe in one year we would be able to started up some features from Sweet.

00:22:36.073 --> 00:22:59.913
<v Paul Hudson>But then why did you adopt first base, an apple and standing still? Now there will be working extremely hard between now and G. M. You know the poor Swifty Whiting. I'm sure working every possible our every day get stuff done. But then next year we presume you see Swifty wire collection, views or safety. Why other stuff? You know, I don't know about that, Not the way I was 14 to get this stuff. You're always waiting for the next sort of thing. Really?

00:23:00.013 --> 00:23:50.244
<v Kateryna Gridina>Yeah, that's true. But in the same time, like because we want to cover as many users as we can, we can take a risk to create at least measure features. Maybe we can start to create, like, something experimental. So even if they're not, every user is moved to the newest version that we can create something like 60 I interface. But like crucial feature like check out, for example, it's not possible because we'll be. I want everybody to use it and I guess, with them adoption of the new technology. It's always risky, always want more stability. You always want to have better interface. You always want to be sure that whatever you develop will work in an hour. And I guess not everyone bringing to take this risk.

00:23:50.534 --> 00:23:51.384
<v Paul Hudson>We were all

00:23:52.974 --> 00:24:09.694
<v Paul Hudson>so surprised. Maybe I don't want you to do this. Well, one more thing. There's always one thing. If I didn't say on Twitter. I think Greg made a joke out of it. You know, I only wish that suits your images could do remote images because it was so nice to have the right to know. We just blown your mind with this new to captain for a one on one thing.

00:24:10.054 --> 00:24:41.464
<v Erica Sadun>I tend to be very conservative when it comes to making recommendations for adoption of technology. And until very recently I was still saying to people to do object to see, because it's so stable and it's so expressive and you basically can build code and know that it's gonna keep compiling. So when it comes to Swift, you I I'm telling most people you're looking at basically a minimum of a two year outlook that if you wanna have an experimental team, if you're a large enough

00:24:42.504 --> 00:25:26.454
<v Erica Sadun>enterprise that, yes, have an experimental team who starting to build things, starting to learn the technology, so you're going to be ready in two years. But I cannot see before two years jumping on that bandwagon unless you're a single vendor who's willing to take a lot of risk. And who, if your product tanks, well, it's something you can put on your resume. I don't think that many people are going to adopt it because it's not there yet. I wouldn't even say it's in beta yet. I would say it's still on. And because of that, I think a two year outlook is actually a fairly optimistic level for adoption.

00:25:26.554 --> 00:26:30.314
<v John Sundell>Yeah, I guess it depends on the size of the company and the product, like you also say, Erica, like what your willingness to take risks are and what the circumstances are. And ah, 11 thing that you all said there, which I also very much agree with us that I think our focus right now when we look at Swifty Y should be learning and trying to figure out also what kind of patterns we want to use with this new framework, like how we architect ah wraps around it, how we make it work well with our current code base and maybe evolved our current code base so that when swift you I is is possible to adopt in the future, it will be easier to do so that we have structured our models and our logic in our AP eyes to work well on dislike declared of New World. I think having that approach like more that learning mindset and experimental mindset rather than you know, taking all your code that you've already written in you like it and throwing it away and starting from scratch was with you. I I think, like having that learning my set is a little bit more healthier approach in most cases.

00:26:30.394 --> 00:26:53.104
<v Paul Hudson>Honestly, im very tired. All number of folks who e mailed me saying, Paul, how do I influence the coordinator pattern in Swifty? Why? Bad question. I understand why they're asking you, but the point is, I simply don't know. I'm writing so much code, trying things out, throwing away so much, coating that that really sucked. That's a terrible idea throwing away. And

00:26:53.104 --> 00:26:53.564
<v Kateryna Gridina>that's how you

00:26:53.564 --> 00:27:11.824
<v Paul Hudson>learned on that. We did. You know, 10 years ago, when I first came out, we weren't trying exactly figuring out what it meant. And only, you know, in the last 45 years have we seen these very mature patterns coming along a lot of wrong parts to get there s Oh, yeah, definitely. We're the noodling around having fun stage.

00:27:11.854 --> 00:27:49.294
<v John Sundell>Yeah, absolutely. And I think one thing that you bring up there also is that there's a tendency to bring your patterns that you already know, like the coordinator pattern or NBC, or whatever pattern that you're used to, and just blindly apply that to this new framework. Or really try to make this framework do the pattern that you are used to. And I think perhaps it's better to start with them or like blank slate in terms of your patterns and the things that you want to use and try to find things that work very well in this new world, instead of just trying to use the old patterns and just make them try to make them work, like shoehorning them into swift You I

00:27:49.514 --> 00:27:53.454
<v Erica Sadun>I'd argue that reactive patterns have been out long enough

00:27:53.964 --> 00:28:24.580
<v Erica Sadun>that there are in the industry, if not necessarily in the Apple umbrella. Some really good experience is using it, and that we're going to see people really adopting things that our industry standard. I'm not really terribly concerned about specific patterns, Maur than I am about how Apple has very clearly said that it intends to provide bridges.

00:28:25.250 --> 00:29:06.830
<v Erica Sadun>It has given us some bridging protocols, but I know from experience that a lot of times it takes them 3456 different tries until they get it right. So the current approach, which, by the way, broke in the latest beta, is not one I expect to see at the end of this year. It is that was up there. There's a protocol and you adopt the protocol and you create an embedded coordinator and so forth. And it provides the bridge that goes between you, Iike it and, um, swift you I am back. It's well documented. It's completely broken. It's beautiful, but

00:29:06.840 --> 00:29:08.190
<v Kateryna Gridina>it's not gonna be the one

00:29:08.190 --> 00:29:23.100
<v Erica Sadun>will end up with. And again, doesn't matter how we get to reactive. I don't think we're going to do anything but hybrid for awhile with how much existing tech

00:29:23.660 --> 00:29:39.170
<v Erica Sadun>that we have and that existing tech is overwhelming. And unless you're willing to start brand new, then you are going to be running into this turbulence between your existing tech, your existing patterns and

00:29:39.350 --> 00:29:41.710
<v Erica Sadun>the new technology. That's what do I offers.

00:29:41.740 --> 00:29:57.160
<v John Sundell>All right, this has been a really interesting discussion about what do you say? Should we round off with just the some very quick final closing statements around how we feel about Swift. You I going forward. So why don't you kick us off? Paul

00:29:57.270 --> 00:30:52.925
<v Paul Hudson>II am extraordinarily exciting. 50 where I think they're coming across in my writing and wear tweet on Dhe. The fact that I'm speaking about next week at my event, I'm loving it. They've done a wonderful job. I am really appreciative to the team with work done on dhe. I hope that comes across my writing that I am genuinely excited about this new direction from Apple having a lot of new things to play. That's always fun. I do enjoy that feeling of being new and sparkly and fresh and exciting and discovery. It's like charting the oceans here a long time ago. But this is this is like This is round one. This is the first version of this witness's gets so much better as the teams are lying as sweating spiritually closer as the other frameworks weigh in with an award Web kit. Look with a really great with the wire Heard what Mac? It looked like that everything would come together. This is the very first version. I'm already very, very impressed. I'm really reporting Lady Next cool.

00:30:52.965 --> 00:31:04.195
<v Kateryna Gridina>I wanted to add that I'm really looking forward for more control over view, positioning about animation, that we can apply for views about

00:31:05.015 --> 00:31:26.135
<v Kateryna Gridina>different properties that we can have. Andi I also wish to have a little bit better documentation because sometimes it's driving me crazy how everything described. But I also very, very, very appreciate their job. And I guess you guys did a lot off cool things there and I'm looking forward for, but they will come up with next.

00:31:26.225 --> 00:31:29.905
<v John Sundell>Awesome. And what about you, Erica? What? What? You're closing thoughts for this episode.

00:31:30.105 --> 00:32:17.595
<v Erica Sadun>I am ridiculously excited about Swift You I It is the most adorable puppy, and I want to take it home and love and snuggled and call it George. I tell you, I have generally avoided going with third party things simply because I try to keep all my writing and all my development dependency free. But if Apple had to adopt a technology and bring it under the umbrella and give it to us with their blessing, I couldn't be happier that this is the one that they chose to give to all of us. And I am so excited to see where it is going and what it's going to give us in terms of development and expressiveness.

00:32:18.065 --> 00:32:19.705
<v Paul Hudson>What about you, John? Well before, too.

00:32:19.815 --> 00:33:41.665
<v John Sundell>I am also really, really excited about Swifty y and like I mentioned, mostly because I feel like it has reignited my excitement and passion for building you eyes. And now that I'm like playing around with the A P I and I am, you know, the playing around with a different types that exists and how we can construct different types of you wise and animations and things like that. Like I'm having a lot of fun. So that aspect is really important to me. And then the second aspect, it's really how it's moving the swift language forward in general. And we talked about that like both from in terms of some of the challenges and opportunities that that brings. But the fact that we're now getting and Maur D s l capable swift and lots of new features around that is really exciting to me also for other domains, not only for swift, you I so I'm excited both about it from a point of view that I'm going to use it, but also what it means for Swift as a language going forward as well. So really good times. All right, but we've now reached the end of this episode. I hope you enjoyed our initial thoughts and discussions about Swifty. Why? I'm sure we're going to bring it up again on this podcast many, many times on future episodes. But for now, I want to thank my panel of guests for joining me on this episode. Pole, thanks so much for being here. If people want to find you and your work and talk to you online, where should they go?

00:33:41.845 --> 00:34:28.233
<v Paul Hudson>Work in fire and Twitter? I am two straws, but honestly, I don't put anything here. If I could, I want to use this time to speak specifically to a handful of people on if they listen to this very blown away. It's Jacob, Kyle, Luca, Raj, Matt, Nate, John, Dave, Kevin and Taylor, who are the handful of folks who have, I know for sure publicly were where they worked on Swift U I s a rather plenty my stuff. I want to plug them because these folks have worked so extraordinarily hard. You've really given up so much time effort on patients and swearing, I'm sure get this thing shipping Onda as much. I love my own work. I am just so admiring of what? They've pulled off and I'm just so excited. What? See that come from next? Amazing.

00:34:28.373 --> 00:34:33.123
<v John Sundell>Awesome. And what about you, Katharina? Working people find you. Thanks so much for being here also.

00:34:33.153 --> 00:34:39.203
<v Kateryna Gridina>Thank you, John, for inviting Thank you folks for being my partners in crime.

00:34:39.913 --> 00:34:56.353
<v Kateryna Gridina>You can find me and Twitter. Also. My name is greed and a ah nde. I'm not that good property this bull. I cannot find any other people too. Thanks for, but yeah, thank you. Everyone who will listen and who plan to this in this podcast

00:34:56.463 --> 00:35:02.083
<v John Sundell>Excellence and Erica Sadun. Thank you so much for being here and working. People find your fine work.

00:35:02.093 --> 00:35:05.843
<v Paul Hudson>The studio I

00:35:05.853 --> 00:35:07.463
<v Erica Sadun>could be found on Twitter as

00:35:07.883 --> 00:35:53.473
<v Erica Sadun>Erica Sadun because I really have no imagination whatsoever. And I just want to say that a lot of times we complain about things like fortune cookie ever messages and so forth. But oh, it is such a privilege to be able to have access to this tech and to be part, even if it is just as an audience to this direction that the language and the technology is taken. And everybody who is developing this inside of Apple, everybody who is on the swift evolution team, we give you grief. But men, we are really, really, really grateful for everything you're doing. So thank you, guys.

00:35:54.253 --> 00:35:54.643
<v Erica Sadun>Yeah,

00:35:54.653 --> 00:36:33.443
<v John Sundell>Yeah, I would definitely. Second that a swell big thanks to the swift, you Why, team? And to everyone at Apple really who contributed to this enormous WWC with so many cool announcements and great new AP eyes and technologies that we can use to build also maps so big, thanks from all of us, you can find me on Twitter. I am at John Sindel and confined my writing, my podcast and lots of other things at Swift bison dele dot com. And you can find everything about this podcast at the Swift community podcast website and as well as our get hub depository and links. All of those things will be in the show notes. But that's it for this episode. So thanks so much for listening. Everybody
