# HIP-23 [Signalling][Phase 2]: Snapshot Administration
### Simple Summary

This proposal propose to have board members put proposals to vote on the snapshot page while providing a protection in case board members or Snapshot were to censor proposals.

### Motivation
Currently anyone can create snapshot polls cluttering the interface and it is likely to dilute the attention of voters. This has already been used multiple times by people to get some "free advertisement" space.
For example we get: 
- [Proposals with wrong duration](https://snapshot.org/#/poh.eth/proposal/QmWnfjekBUgWdMTGFMgmEYx9M4rHZLM96GPgqS5GDDmLN8).
- [Proposals marked as signalling which are not (wrong duration, no forum post to debate)](https://snapshot.org/#/poh.eth/proposal/QmVV6zGqmy3qBYjh9opcm8a1v6CdEq3cgD1BBR1Kt6yPsb).
- [Old tests popping up](https://snapshot.org/#/poh.eth/proposal/QmcofBqf2MMMjXzA8j8UZanxCPY7iNe42Pk5JNNiSobrhC).
- [Outright spam](https://snapshot.org/#/poh.eth/proposal/QmT5vZKty5mhoxwVxTtvUeucvUKomVqfdYb8FVST8mN43s).



### Specification

- The main snapshot page is reserved for official proposals (following HIP-5 and its possible amendments).
- Only board members and their delegate can technically create proposal there.
- After being informed of a proposal request, a board member or delegate must verify that it complies with HIP-5 (and its potential amendments), if it does, he puts it to vote without delay. Board members do not have any discretion in whether a proposal is put to vote or not. It is a purely administrative task to avoid spam / invalid proposals from cluttering the interface.
- In case a valid proposal were not to be put to vote within a week by any board member or delegate, anyone can create a new snapshot page with a 10 days proposal changing the board composition and the official snapshot page. It should include "Make no change" and "Change the board composition and snapshot page". It should also be displayed on the forum.
A board member can also post this proposal on the current snapshot page.
If the amount of "Change the board composition and snapshot page" votes on any of the snapshot page exceeds the amount of "Make no change" on both snapshot pages, the proposal changing the board and snapshot page is accepted.
In case no proposal is created by a board member within the voting period of the proposal on the new snapshot page and the amount of "Change the board composition and snapshot page" exceeds the amount of "Make no change", the proposal changing the board and snapshot page is also accepted.
- In case of proposals/votes being censored by snapshot a similar process can be used to change the voting platform to a new platform (in this case the board composition isn't changed).
- A Proof Of Humanity polls snapshot page can be created for non enforcing polling.
