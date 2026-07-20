## Mao
# VIEW THIS IN PLAINTEXT/CODE MODE

	# Golden Rules
	
- Mao has many rules. The only rule that may be revealed is this one.
> Mostly a holdover from generic Mao, but I think I still want this.
> It encourages the philosophy that the game should still be simple enough
>  that anyone should be able to sit down and pick up on what is going on.

- Every action is forbidden except those that are explicitly permitted.
> The most important thing to note is that you can still do things that are forbidden.

- If a forbidden action is taken, any cards involved in the action are moved to the offender's hand.
	  The offending player must also draw a card.
> Sometimes, this punishment is worth it.
> Hmmm, maybe it's too worth it. Two cards for a violation instead?

- The State may do what it pleases.
> Anything that involves the running of the game in general is done by The State.

- All rules apply to all players at all times.
> this mostly applies to any rules that refer to "you"

- If an action is written in the passive voice, the action is performed by The State.
> This can cause some templating issues. Too bad!

- If an action is written as a command, the action is performed by whichever player the rule is relevant.
> kinda ass wording because of the "all rules to all players" thing
> also need to mention that any action taken as a result of a rule card is always allowed, but is still listened for.


	# Tags

- Tags are qualities that can be given to cards.
- Each tag has a unique identifier (either a name or a symbol, preferably both)
> the name is needed when referring with rule cards, symbol is needed when giving the tag to a card.

- Tags appear surrounded in square brackets e.g. [Ace], [A]
> not sure if i want to keep the square brackets around the names (i.e. Ace, [A] )

> still need to talk about tag comparison

> and compound tags

> and special tags like Wild

> and special designations of Tags, like rank or suit


	# Cards
	
- Cards are the primary game object of Mao.

- Each unique card has a name. Any card with this name is a copy of this card.
> this is basically Plato's Theory of Forms, or Oracle Text in MtG.

- A card may have any number of tags.
- If a given tag would be added to a card that already has that tag, it is not added.
> e.g. if an effect would give the Three of Diamonds a [Three], it would not do so.

- A card may have any amount of Rules Text.
- A card's Rules Text applies whenever it is inside the Rules Zone, or while it is on the top of the Play Pile.
> still need to think about this one, the relevance is for "When this card is played..." clauses

> mention front and back faces?


	# Basic Operations
> not sure if this section is needed?
> but needs to be defined for the moment.

- To draw, take the top card of the Draw Pile and add it to your hand.

- To play, take a card from your hand and put it on the top of the Play Pile.

- To pass, indicate in some way that you are passing. It stops being your turn and the next player begins their turn.
> need to define who is "next"
> maybe have another section for this?

- To tuck, take a card and put it on the bottom of the Draw Pile.

- To reveal, choose a card and make it public to all players.

- To return, take a card and put it on the top of the Draw Pile.
> still iffy on this one.

> maybe add cycle at some point?


	# Rule Cards

- Rule Cards are that are created by the players during a game.

- Rule Cards should be visually distinct from regular cards.
> dont think i still want this, but still here for now.

When a Rule Card is approved, it is moved to the Rules Zone.
> i think approval works here?
> only just thought of this but this makes sense.
> Note! Approval is the determination of whether a card is valid (usually compared to the next one down).
> we do NOT care if the players like it or not (yet)

[5.3] Rules Text on the front face of a card only applies when that rule is inside the Rules Zone.
[5.4] Rules Text on the back face of a card applies at all times.
> still iffy on these
> feels kinda wrong idk


	# Basic Rules of Play
	
- The following rules begin active at the start of the game:

- If it is your turn and you have not played a card, you may play a card from your hand.
- If it is your turn and you have not drawn a card, you may draw a card.
- If it is your turn and you have drawn or played a card, you may pass.

- If you have one card in your hand, you must call "Mao" when you pass.

- You may play cards from your hand with the same name as the card on the top of the Play Pile.

- If you pass and you have no cards in your hand:
	Add 1 to your Score.
	You may either:
		- Create a Rule Card and move it to either the Rules Zone
  		- Look at a card in the Rules Zone.
	Draw X cards, where X is 3 + your Score.

- If you pass and you have 10 or more cards in your hand:
	Subtract 1 from your Score.
	Tuck half your hand (rounding up) at random.
> cannot punish players for 'losing' too harshly, maybe change this for 1v1

- If you pass and no card has been approved since it was last your turn, the top card of the Draw Pile is placed onto the top of the Play Pile.

- If the Draw Pile has no cards, all but the top card of the Play Pile is moved to the Draw Pile, then the Draw Pile is shuffled.


	# Approval and Denial
> The Audit exists because I wanted to expand the design space of the cards.
> The idea is that some effects are too powerful to be recurred.
> If these effects had a "When this card is played...", they still get their effects off even when its not a valid card.
> This is especially dangerous when the effect forces an opponent to draw a card, as they can effectively deny someone from EVER winning.

> Approval means that an effect only normally happens once. (of course, it can still be reccured by other means)
> What Tags it has is now important because it affects how easy it is to access the effect.
> A card may be incredibly powerful, but it might be locked away under [2 & Club].
> This is the safest way to include clauses that give other players cards.

> Denial means that an effect is repeatable, but you must effectively skip a turn to use it, the same way as if you had no playables and just had to draw.
> In fact, it's even worse, because it uses your turn's play too.
> But in return, you can get your effect. These should be card selection effects, but there can be some other things here too.
> Here, the tags become relevant in that if the top is playable, you must decide if you want to get rid of your denial card.
> Notably, you do not want to be left with a denial card as your last card, as opponents likely know what it is because theyve seen you play it.

> There is probably also some space to be played with a card that has BOTH approval and denial clauses.
> This sort of card probably has its denial clause working towards its approval clause, like idk:
> "Sample Text" - [♥]: When this card is denied, search for a Heart and put it on top of the Draw Pile - When this card is approved, you may play any Hearts you have.

- When a card is played, it is audited.
> this is the check that sees whether the card played is valid.
> !!!! This effect needs to apply LAST (i.e. it is always first on the stack) to work as intended.
> Note that if the card is removed from the Play Pile before the audit happens, it does not get audited.
> Also note that even if the card is moved inside the Play Pile, it is still audited.

- To audit, compare the auditee's tags to the tags of the card directly below it. If they share a tag, approve it. if they do not, deny it.
- If a card is denied, it is returned to the hand of whoever played the card. That player draws a card.
> this is templated very much like the 'forbidden action' golden rule, which is because it is that rule.
> there might be a way to make it work, but i'm not sure...


	Calls

	Speed of Play

	The Stack



