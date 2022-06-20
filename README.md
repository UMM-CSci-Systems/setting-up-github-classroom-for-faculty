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
GitHub Education benefits for teachers. I've never done this (didn't
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

For each lab you need to:

- Add the assignment in your GitHub Classroom
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
  - 

## Shutting it all down

When the semester is over you should probably archive the classroom
so that it's clear that it's no longer an active workspace. We should
probably also be archiving all the individual repositories, but that's
a huge amount of work, so I wouldn't bother. I am working on creating
a tool to automate that process, though, and if I get that going then
it would make sense to use it when the semester's over.
