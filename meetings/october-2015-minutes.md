Agenda: https://github.com/rdfjs/rdfjs.org/wiki/Meetings#october-2015
elf-pavlik 18:59
scribe: @Acubed
Acubed 18:58
@elf-pavlik (To @Acubed) if you can try to capture what people are saying
elf-pavlik 18:59
chair: @elf-pavlik
we start in 30 sec
TOPIC: online group collaboration spaces (max 10 min)
Acubed 19:01
@elf-pavlik: The first topic to go through... tools to use for online collaboration. Let's +1/-1 various tools. For chat... Gitter/IRC?
RubenVerborgh 19:01
Gitter: +1
bergos 19:01
gitter: +1
l00mi 19:01
Gitter:+1
Acubed 19:01
IRC: +1
gkellogg 19:01
IRC: +1, +.5 for Gitter
rivettp 19:01
Gitter+1
l00mi 19:02
Github:+1
gkellogg 19:02
Github: +1
Acubed 19:02
@elf-pavlik: And for wiki there's W3C and GitHub.
RubenVerborgh 19:02
Github:+1
Acubed 19:02
MediaWiki:+1
bergos 19:03
github: +1
elf-pavlik 19:03
Github: +1
Aklakan 19:03
github : +1
Acubed 19:04
@elf-pavlik: Next point, Website. rdfjs.org. Reference the W3C community group from the website, use the website?
gkellogg 19:04
rdfjs.org: +1 You can probably use a CNAME to redirect to GitPages.
RubenVerborgh 19:04
domain name +1, but website has to be managed by community, for instance GitPages
Acubed 19:04
@RubenVerborgh: Domain name is fine, but
... website should be run by community
l00mi 19:05
right now if not mistaken it is already pointing to github ip
RubenVerborgh 19:05
-1 on task forces choosing
(should all use the same thing)
Acubed 19:05
@elf-pavlik: Task forces can choose their own collaboration space?
@RubenVerborgh: We should avoid fragmentation and use the same thing
@elf-pavlik: Start a new repo?
@RubenVerborgh: Current group seems to be good
RubenVerborgh 19:07
+1 for hangout: everything is going well
gkellogg 19:07
Hangouts: +1
Acubed 19:07
@elf-pavlik: To Teleconferences. Any objections to hangouts, or any alternatives?
bergos 19:07
hangouts: +1
l00mi 19:07
hangouts: +1
Aklakan 19:07
hangouts: +1
ericprud 19:07
hangouts:+1
elf-pavlik 19:08
hangouts: +1
Acubed 19:07
No opinion
rivettp 19:07
hangouts +1
Acubed 19:08
@elf-pavlik: I have access to rdfjs on Twitter, if someone is interested in accessing the account I'm open to sharing credentials.
elf-pavlik 19:09
workstreams (actionable) (max 40min)
Acubed 19:09
... Collaboration is very exciting. First item is representing triples
elf-pavlik 19:10
Proposal: Representation Task Force
please use q+ / q- for entering the queue
Acubed 19:10
@RubenVerborgh: Thomas and I had a good chat yesterday... We propose a task force for discussing technical issues and low-level APIs
elf-pavlik 19:11
https://github.com/rdfjs/rdfjs.org/wiki/Representing-triples-and-quads
l00mi 19:12
q+
ericprud 19:12
q+ to ask if folks are leaning towards data or function access
elf-pavlik 19:13
ack @l00mi
Acubed 19:12
@bergos: Discussions on how to bring together the various high-level APIs from a common low-level API/representation
elf-pavlik 19:14
ack @ericprud
Acubed 19:15
@RubenVerborgh We're talking about an in-memory representation... there's several Turtle parsers, each of them outputs in different ways. What we're trying to achieve is a common data format for output
elf-pavlik 19:16
@gkellogg: explains how it works in ruby-rdf
Acubed 19:16
@gkellogg: The way we do it in Ruby is we define an interface... it yields the triples or quads it generates.
RubenVerborgh 19:17
https://github.com/promises-aplus/promises-spec
https://github.com/promises-aplus/promises-tests
Acubed 19:18
@RubenVerborgh Promises seems to be the common interface being adopted
+q Parsing documents asynchronously/synchronously
RubenVerborgh 19:18
I meant: the promises spec is a good example of how we can standardize an interface
elf-pavlik 19:20
@Acubed I will ack you next!
and scribe what you say
ack @Acubed
@Acubed: we have rdf-interaces and I know Turtle library which uses its output, it takes the whole document and calls callback with all the triples
RubenVerborgh 19:21
q+ to clarify promises and why RDF interfaces is not sufficient
ericprud 19:21
q+ to ask what use cases we know of
elf-pavlik 19:22
... asynchronious implementations send document all at one (scribe missed it)
@bergos do you ask where do we need promisses?
@Acubed what features do you see rdf-interfaces is missing?
Acubed 19:22
@Acubed: We already have RDF Interfaces, which features is it missing?
elf-pavlik 19:22
@bergos quads, async parsers
vanthome 19:22
Where is this matrix?
bergos 19:22
https://github.com/rdfjs/rdfjs.org/wiki/Representing-triples-and-quads
elf-pavlik 19:23
@ericprud still on the q?
RubenVerborgh 19:23
+1 on what bergi is saying
Acubed 19:23
@bergos: Let's continue to collect a list of use-cases
elf-pavlik 19:24
ack @ericprud
Acubed 19:24
@ericprud Trying to understand the use-cases we have already... Is there anything else?
elf-pavlik 19:25
http://www.w3.org/community/rdfjs/wiki/Comparison_of_RDFJS_libraries
RubenVerborgh 19:25
Clarification of earlier point: RDF Interfaces is not JavaScript-idiomatic; we want a JavaScript way to interact with triples and quads on a low level.
Being JavaScript-idiomatic includes support for asynchronicity.
Acubed 19:26
https://www.w3.org/community/rdfjs/wiki/Comparison_of_RDFJS_libraries
ah
elf-pavlik 19:26
ack @RubenVerborgh
rivettp 19:26
it seems to me there might be value in mapping rdf:type info into Javascript classes - e.g. using Shapes
elf-pavlik 19:27
Next steps, and how people can engage
Acubed 19:28
@elf-pavlik What's the next step here?
@RubenVerborgh Figuring out how to represent triples
RubenVerborgh 19:29
Task: bergi & Ruben send out mail to recrute for Representation Task Force
elf-pavlik 19:30
Next topic (very quick) Use cases (see Task Force)
nicola 19:29
(room is full I cant' join)
RubenVerborgh 19:29
=> that's a problem for using Hangouts!
Acubed 19:30
D:
elf-pavlik 19:30
oh shit! sorry @nicola
nicola 19:30
(I have been following here anyway)
elf-pavlik 19:30
next time we need to do it on air!
nicola 19:31
(I was going to help facilitating but you are doing super well)
Acubed 19:31
@elf-pavlik If someone is interested in listing use-cases step up
RubenVerborgh 19:31
in the meantime, I created a Tasks page: https://github.com/rdfjs/rdfjs.org/wiki/Tasks
Acubed 19:31
@Acubed: I can help
nicola 19:32
(is someone scribing?)
Acubed 19:32
(me, badly)
@elf-pavlik Who's using user interface libraries with RDF?
@Aklakan ... making SPARQL queries, converting to JSON
rivettp 19:33
RDF Shapes work provides basis for building UI forms etc
RubenVerborgh 19:33
We have these UIs
http://client.linkeddatafragments.org/
http://git2prov.org/
http://everythingisconnected.be/
Acubed 19:34
Is antoniogarrote here?
RubenVerborgh 19:34
And actually also
http://fragments.dbpedia.org/2015/en (server-side JS)
vanthome 19:34
Yea, in RDF shapes, I see big potential in generating UIs
RubenVerborgh 19:34
Also, there's the Hydra console: http://www.markus-lanthaler.com/hydra/console/
vanthome 19:34
This include shacl
elf-pavlik 19:35
Next TOPIC: Mapping Projects (dependencies, maintainers/contributors, specs, features) 
RubenVerborgh 19:35
Hydra, in general, has lots of UI potential (similar to SHACL)
ericprud 19:35
q+ to blather about validation
Acubed 19:35
@l00mi: Using RDF Shapes to generate user interfaces/forms, experiences on mobile
... having a common representation in memory would be helpful for performance
ericprud 19:35
http://www.w3.org/2013/ShEx/FancyShExDemo.html?schemaURL=Examples%2FIssue-simple-annotated.shex&dataURL=test%2FIssue-pass-date.ttl&starting-nodes=%3CIssue1%3E&colorize=true
elf-pavlik 19:36
ack @ericprud
Acubed 19:36
@ericprud: I've done some user-interface stuff meant for RDF developers. It detects mistakes. And I have a different set of requirements.
nicola 19:36
(if there is multiple people in the same office with two connection, maybe they could drop, so I can join)
Acubed 19:37
One more use case from me
l00mi 19:37
q+ another use case finally would be to update a graph in the client which then gets persisted on server
kind of syncinc
elf-pavlik 19:38
@nicola I don't think so  sorry for that next time we'll fix it
gkellogg 19:38
A JSON-LD parser would probably have a hard time tagging a line number with a triple/quad, but could do something like a json-path. RDFa can also associate a XPath IIRC
elf-pavlik 19:39
https://github.com/rdfjs/rdfjs.org/wiki/Representing-triples-and-quads#Use_cases and https://github.com/rdfjs/rdfjs.org/wiki/Use-cases or
Acubed 19:39
@RubenVerborgh Compiling a list of how people use RDF libraries on a high level
elf-pavlik 19:40
@Acubed: little project I did a few ago, rendered template with RDFa instructions and filling in variables based on sub graph matching from database
... once you generate this document in will contain the same tripples
... facebook react seams to do something similar
Acubed 19:41
ty
@l00mi: This is something I'm interested in... And the fact the information is reactive is beneficial
Aklakan 19:41
http://js.geoknow.eu/demos/rex/
Acubed 19:42
@Aklakan: I'm working on annotating the reverse, annotating the HTML to persist to the server
(understanding this correctly?)
elf-pavlik 19:43
ack @vanthome (i believe)
Acubed 19:43
@vanthome: Generating a UI automatically... Using a JSON-LD based API, JSON Schema, and a DSL.
... Completely automatically generating UIs
... we've built an implementation based on JSON Schema
... And building a database representation
Aklakan 19:44
@Acubed: Its annotating the HTML forms with RDF specific markup (e.g. rex-subject, rex-predicate, ...) such that the form can be both pre-filled out from existing data in a sparql endpoint as well as persist any changes back to it
Acubed 19:44
ty
elf-pavlik 19:45
TOPIC: Mapping Projects (dependencies, maintainers/contributors, specs, features)
Acubed 19:44
@elf-pavlik: Last topic, mapping projects
elf-pavlik 19:45
http://holodex.enspiral.com/
l00mi 19:45
q+
elf-pavlik 19:46
ack @l00mi
Acubed 19:46
... It was a project not originally using RDF
... I propose a workflow based on that
@l00mi: Why do we want this low-level API to interact?
elf-pavlik 19:48
TOPIC: group charter (max 5min)
Acubed 19:47
@elf-pavlik: I think we can close this, it's exciting we have many different cases
... more boring is taking on a charter
@ericprud: I can help
@elf-pavlik: For now we can just keep adding to the wiki
RubenVerborgh 19:48
https://github.com/rdfjs/rdfjs.org/wiki/Meetings#group-charter-max-5min
elf-pavlik 19:49
TOPIC: misc (max 5min)
Acubed 19:49
@elf-pavlik: Next meetings
l00mi 19:49
q+ Who is at ISWC next week?
RubenVerborgh 19:49
monthly +1
elf-pavlik 19:50
monthly +1
RubenVerborgh 19:49
going to ISWC: +1
elf-pavlik 19:50
ack @l00mi
bergos 19:50
monthly +1
elf-pavlik 19:50
ISWC IRL meetup anyone ?
Acubed 19:50
@l00mi: Is anyone going to ISWC, interested in meeting up?
Aklakan 19:50
monthly +1
l00mi 19:50
monthly +1
elf-pavlik 19:51
http://iswc2015.semdev.org/
Acubed 19:50
@elf-pavlik: A face-to-face is good
@RubenVerborgh: Last ISWC had 70 people... but this time we had to cancel for insufficient interest
... not the best feeling to be suddenly ignored, we need to figure out how attract interest
elf-pavlik 19:52
TOPIC: group chairs
RubenVerborgh 19:52
I'd volunteer as a chair
l00mi 19:52
Task associated?
Acubed 19:52
@elf-pavlik: Last topic, group chair. Groups don't have to have chairs, but it's useful.
elf-pavlik 19:52
+1 @RubenVerborgh
RubenVerborgh 19:52
(if needed)
elf-pavlik 19:53
animating group 
l00mi 19:52
+1 @RubenVerborgh
RubenVerborgh 19:52
(and co-chairs are welcome )
gkellogg 19:52
@elf-pavlik is doing a great job.
bergos 19:53
i can co-chairs
l00mi 19:53
co-chair @elf-pavlik
gkellogg 19:53
Having two chairs is always a good idea
elf-pavlik 19:54
@RubenVerborgh what we want to ask the whole group?
Acubed 19:54
@RubenVerborgh I think it's a good idea to have chairs regardless of who they are... let's compose a mail to everybody
@elf-pavlik: I can take the minutes and post to the wiki
@RubenVerborgh: I'm busy at ISWC, but I can help
elf-pavlik 19:56
@bergos what do we do about limit of he hanout?
RubenVerborgh 19:56
WebEx then?
Acubed 19:56
@bergos: We have a 10-person limit which we reached... what other possibilities do we have?
RubenVerborgh 19:56
+1 for WebEx instead (always had good audio quality there)
Acubed 19:56
@ericprud: I can setup a WebEx with 10 seconds of warning
melvincarvalho 19:56
+1 @bergos chair
Acubed 19:56
... Some police of abuse might be necessary
@bergos: I've had problems with things on Linux, will WebEx work?
melvincarvalho 19:57
ive not got webex working on linux yet, but I sometimes dial in thru skype
elf-pavlik 19:58
one can use G+ Hangout to call +1
Acubed 19:58
@ericprud: It works on my platform... And you can dial into it
melvincarvalho 19:58
would be nice to build our own webRTC solution 
Acubed 19:58
@melvincarvalho++
elf-pavlik 19:59
https://www.w3.org/2006/tools/wiki/WebExFAQ#Can_we_use_international_phone_numbers_for_WebEx.3F
 The only call-in number supported by the MIT/WebEx instance is the one with the +1 country code: +1.617.324.0000.
RubenVerborgh 19:59
+1 for WebEx
elf-pavlik 20:00
+1for WebEx
Acubed 20:00
@elf-pavlik: So do we all agree next time using WebEx?
bergos 20:00
webex: +1
Aklakan 20:00
+1 WebEx
Acubed 20:00
@ericprud: Someone just has to remind me
vanthome 20:00
+1 let's test and see. If new problems occur we can try talky.io
nicola 20:00
+1 agree w/ @vanthome
RubenVerborgh 20:01
@elf-pavlik We'll be in touch by mail for the summary e-mail
Acubed 20:01
@elf-pavlik: Ruben will send out the summary on Sunday... thanks everyone
l00mi 20:01
Most impressed by the time-boxing! Thanks @elf-pavlik
elf-pavlik 20:02
Great call, Thanks everyone 
