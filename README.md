# Setting up GitHub Classroom, etc., for faculty <!-- omit in toc -->

This is a brief guide for how we set up and use GitHub Classroom
when teaching Computer Science lab classes at the University of Minnesota
Morris.

- [Create a GitHub organization](#create-a-github-organization)
  - [Optional: Upgrade your organization](#optional-upgrade-your-organization)
  - [Optional: Make a logo](#optional-make-a-logo)
  - [Add your TA(s) as members of the organization](#add-your-tas-as-members-of-the-organization)
  - [Maybe?: Add the students as members of the organization](#maybe-add-the-students-as-members-of-the-organization)
- [Create a GitHub Classroom](#create-a-github-classroom)
- [Optional: Set up Slack organization](#optional-set-up-slack-organization)
- [Setting up individual labs](#setting-up-individual-labs)
  - [Add the assignment in your GitHub Classroom](#add-the-assignment-in-your-github-classroom)
  - [Add the invite link to Canvas](#add-the-invite-link-to-canvas)
- [Shutting it all down](#shutting-it-all-down)

## Create a GitHub organization

The first step is to [create a GitHub organization](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch) 
using the "Free" Tier for this particular
semester of the course. This will hold all the student repositories in
a single place, which makes it easier for both faculty and students to
keep track of things. We've typically used a specific naming scheme
to make it easier to find things. In Systems Practicum (CSci 3412),
for example, we've used <https://github.com/umm-csci-3412-fall-2021>.

### Optional: Upgrade your organization

[This guide to GitHub Classroom](https://github.blog/2020-03-18-set-up-your-digital-classroom-with-github-classroom/)
suggests that you can upgrade your GitHub organization with
GitHub Education benefits for teachers.  The relevent directions (as of 6/20/2022) from that link state

```
When creating a new organization, choose the free plan option. Then, you can find the offer to upgrade your organization in the GitHub Teacher Toolbox listed under GitHub as “Self-serve free Team plans to academic organizations you own.”
```

I've (Nic) never done this (didn't
know it was a thing until now), but it looks like one benefit would
be that it allows the students to have private repositories.

:warning: I have tried setting student repos in GitHub Classroom to
private before, and we almost immediately used all the free credits
for GitHub Actions. Given how important GitHub Actions are for most
of the labs, I then went back to using public repos. In a perfect world,
though, it would be nice to give students private repositories and
admin permissions so they can make them public if they want to include
them in an online portfolio.

### Optional: Make a logo

You might find it useful to create a logo for this semester's course.
As someone who's taught this course _many_ times, I've found it helpful
to have a slightly different logo each semester to make it easier to
distinguish different semesters.

:bangbang: Nic should upload the "starter" image and say something
about how he creates the semester specific images. It would even be
cool to automate that process, although I don't know how likely that
actually is.

### Add your TA(s) as members of the organization

Adding your TA(s) as members of the organization will ensure that
they can see all the repositories and have the ability to engage in
things like code reviews. If you are using private repositories
you may need them to be set up as `Owner` (or some other elevated
status) of the organization so they can access the private repositories.

### Maybe?: Add the students as members of the organization

I know that in the early days of GitHub Classroom you had to manually
add all the students as members of the new organization. I _think_ that's
been changed and that GitHub Classroom may automatically add them now,
but I'm honestly not sure.

If you do have to add them, it's a nuisance because you don't know in
advance what their GitHub usernames are. So you'll have to either ask
them before the first lab starts (and hope they repsond to whatever
request you make) or be prepared to add them "on-the-fly" in the first
lab session.

## Create a GitHub Classroom

After you have an organization, you can [create a GitHub Classroom](https://docs.github.com/en/education/manage-coursework-with-github-classroom/teach-with-github-classroom/manage-classrooms)
that uses that org. Again, we tend to use a common naming scheme, like
`umm-csci-3412-fall-2021-classroom`.

In the process of setting up the classroom, one of the questions is what
organization you want to use; this is where you'd plug in the organization
you created up above.

## Optional: Set up Slack organization

We've historically set up Slack organizations for each semester of
our lab courses as a way for students to talk to us and each other about
the labs. If you're so inclined, I would definitely recommend it.

I also use the same logo that I created for the GitHub organization
for the Slack organziation, which helps me and the students keep those
things straight.

## Setting up individual labs

Now that all that infrastructure is set up, you'll need to set up
each individual lab. You could do that all up front, or do it one lab
at a time as the semester progresses. (I always take the latter approach,
but that's mostly due to lack of organization and poor planning rather than
any particular advantage to that process.)

:warning: If you're going to set up the labs on-the-fly, I'd recommend
that you go through all the assignments on Canvas and change all the
GitHub Classroom links to something like `UPDATE_ME` so it's clear to everyone
involved that they're not looking at a working link. Otherwise you'll
probably end up with plausible looking links that point into last year's
GitHub Classroom, which isn't good.

For each lab you need to add the assignment to your Github classroom, and
then add the invite link to Canvas (or whatever LMS you're using).

### Add the assignment in your GitHub Classroom

To add the assignment to the GitHub Classroom hit the big green "Create
an assignment" button.

- You can set the deadline, but I'm not sure it actually does much (or
    or anything).
- Set it as an individual or group assignment as appropriate for the lab.
  - I usually set the "Name your set of teams" field to something like
      "Lab 3 teams", but I don't think it actually matters much.
  - Set the max/min team sizes if you care.
- Set the repo to be public or private as appropriate. :warning: Private
    would be nice, but see the note above about GitHub Actions credits.
- I would probably grant students admin access to their repository.
    They usually don't need it, but every now and then someone finds it
    useful and it's easier to grant it here than have to piecemeal it
    later.
- Use the "primary" repo in the `UMM-CSci-Systems` organization as the
    template repository for the assignment.
  - That repo has to be a _template_ repository. All the existing
      starter repositories in the `UMM-CSci-Systems` organization are
      already template repositories, but if you make a new repository
      for a new lab, you'll need to mark it as a template repository.
  - I've never set up Codespaces or the "Add a supported editor" features.
      Because of the systems programming in this course, and the desire
      to have them use CLI editors at least some, these options probably
      don't make any particular sense for us in this class.
- I've never used the autograding feature. I think that having the
    GitHub Actions tests is probably sufficient to the task for us.
- I _do_ tend to select the "Enable feedback pull requests" option,
    although to be honest we haven't used that very often or coherently.
  - It is sometimes nice to be able to see exactly what they've changed
      from the starter code on some labs, and it's no real work
      to tick the box when you create the lab, so I tend to do it.
  - :warning: For reasons I've
      never really looked into, it seems that GitHub Classroom doesn't
      always actually create that PR, though. We've never used it enough
      for me to both digging ino the problem, though. (It's also pretty
      easy to create a Feedback PR manually if you decide you need one.)

### Add the invite link to Canvas

When the assignment is created you want to click the big green
"Copy invitation link" button to get the invitation link, and then
paste that into the Canvas assignment for the lab.

When the students click that link for a _group_ assignment, they are
asked to either join an existing team or create a new team, so they need
to coordinate with their teammate(s) at that point.

:warning: One advantage of not putting the "real" links into Canvas
too early is that it makes it less likely that a student will create
a bunch of teams at the start of the semester before they know who
they'll be paired up with for those labs.

:bangbang: It is fixable if some students do manage to muddle things up, e.g.,
joining the wrong team, or two people that were supposed to work
together each creating separate teams. It's not trivial, though, and doing
so requires some understanding of GitHub's notion of teams. I can write up
something on that in a separate document if that would be useful.

## Shutting it all down

When the semester is over you should probably archive the classroom
so that it's clear that it's no longer an active workspace. We should
probably also be archiving all the individual repositories, but that's
a huge amount of work, so I wouldn't bother. I am working on creating
a tool to automate that process, though, and if I get that going then
it would make sense to use it when the semester's over.
